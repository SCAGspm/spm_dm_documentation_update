# How to add a Global Reference layer
### 3 main components:

1. prepare data for import
2. update UrbanFootprint code
3. rebuild database

***Assumptions***

- new layer is in a single table in your local postgres database
- this table has a column `wkb_geometry` of type geometry that represents geospatial data that will render on a map


## Prepare Data for Import

1. prep your source data table for import
    - name your source data table `scag_<name_of_reference_table>`
        - source table names must start with the word `scag_` as defined in the
         `scag_dm_config_entities.py` file's  `ScagDmConfigEntitiesFixture` class's `regions` method `key='scag'`
        - i.e. tablename = `scag_flood_zones`
2. example schema for `scag_flood_zones`

        scag_spm=# \d scag_flood_zones
                  Table "public.scag_flood_zones"

            Column    |          Type          | Modifiers
        --------------+------------------------+-----------
         wkb_geometry | geometry               |
         fld_zone     | character varying(100) |

## Update UrbanFootprint Code

1. create the unique db entity key
    - in the `scag_dm_config_entities.py` file's `ScagDmDbEntityKey` class, add the unique key
        - i.e. `FLOOD_ZONES = 'flood_zones'`
        - this lowercase `'flood_zones'` must match the
         `<name_of_reference_table>` from your source data table
        - `FLOOD_ZONES` must be a unique key
2. create the django model class
    - in the `urbanfootprint/footprint/client/configuration/scag_dm/base` directory, create a new python file:
     `<name_of_reference_table>.py`
    - import models and Feature at the beginning of the file (as seen below)
    - name your class the camelcased version of `<name_of_reference_table>` i.e. `FloodZones`
    - define the attributes from your source data table that you would like to see in UrbanFootprint i.e. `fld_zone`
        - [django model field type documentation](https://django-document-tchinese.readthedocs.org/en/latest/ref/models/fields.html#field-types)
    - add the Meta class within the main feature class
    - example: `flood_zones.py`

            from django.contrib.gis.db import models

            from footprint.main.models.geospatial.feature import Feature

            __author__ = 'calthorpe_associates'

            class FloodZones(Feature):
                fld_zone = models.CharField(max_length=50, null=True)

                class Meta(object):
                    abstract = True
                    app_label = 'main'

3. create the dbentity in `scag_dm_region.py`
    - import the django model class at the top of the file
        - i.e. `from footprint.client.configuration.scag_dm.base.flood_zones import FloodZones`
    - define the dbentity in the `ScagDmRegionFixture` class's `default_db_entities` method's return statement's `FixtureList`
        - example: `flood_zones`

                class ScagDmRegionFixture(RegionFixture):
                    ...
                    def default_db_entities(self):
                        """
                            Region specific db_entity_setups
                        :param default_dict:
                        :return:
                        """
                        ...
                        return default_db_entities + FixtureList([
                            ...
                                update_or_create_db_entity(config_entity, DbEntity(
                                    key=Key.FLOOD_ZONES, # matches unique db entity key
                                    feature_class_configuration=FeatureClassConfiguration(
                                        abstract_class=FloodZones # matches django model class name
                                    ),
                                    feature_behavior=FeatureBehavior(
                                        behavior=get_behavior('reference'),
                                        intersection=GeographicIntersection.polygon_to_polygon
                                    ),
                                    _categories=[Category(key=DbEntityCategoryKey.KEY_CLASSIFICATION, value=DbEntityCategoryKey.REFERENCE)]
                                )),
                            ...
                        ])

4. define the default style for the layer in `scag_dm_layer.py`
    - in the `ScagDmLayerConfigurationFixtures` class's `layers` method's return statement's `FixtureList`
    add the `LayerConfiguration` for the new layer
    - Note: there are three geometry types that can be styled: polygon, line and point

        |	geometry_type	|
        |	------------------	|
        |	POLYGON	|
        |	POINT	|
        |	LINESTRING	|

    - there are two default style types: single and categorical
        - example of a polygon geometry with a single style type:

                LayerConfiguration(
                    library_keys=[LayerLibraryKey.APPLICATION],
                    db_entity_key=ScagDmDbEntityKey.ENDANGERED_SPECIES,
                    layer_style=dict(
                        geometry_type=GeometryTypeKey.POLYGON, # defined geometry type here
                        style_attributes=[
                            dict(
                                style_type=StyleTypeKey.SINGLE, # defined style type here
                                style_value_contexts=[
                                    StyleValueContext(value=None, symbol=None, style=Style(
                                        line_color='#009929',
                                        line_opacity=1,
                                        line_width=3
                                    ))
                                ]
                            )
                        ])
                ),

        - example of a polygon geometry with categorical styles:

                LayerConfiguration(
                    library_keys=[LayerLibraryKey.APPLICATION],
                    db_entity_key=ScagDmDbEntityKey.FLOOD_ZONES,
                    layer_style=dict(

                        geometry_type=GeometryTypeKey.POLYGON, #defined geometry type here
                        style_attributes=[
                            dict(
                                attribute='fld_zone',
                                style_type=StyleTypeKey.CATEGORICAL, #defined style type here
                                style_value_contexts=[
                                    StyleValueContext(value='100 Year Flood Hazard', symbol='=', # define categorical style filter here
                                        style=Style(
                                        polygon_fill='#885ead',
                                        line_color='#d3d3d3',
                                        line_width=1,
                                        line_opacity=0.8
                                        )
                                    ),
                                    StyleValueContext(value='500 Year Flood Hazard', symbol='=', # define categorical style filter here
                                        style=Style(
                                        polygon_fill='#7cb0df',
                                        line_color='#d3d3d3',
                                        line_width=1,
                                        line_opacity=0.8
                                        )
                                    )
                                ]
                            )
                        ])
                ),

5. add layer to client initialization
    - add import statement in `urbanfootprint/footprint/client/__init__.py`
    - example: `from footprint.client.configuration.scag_dm.base.flood_zones import FloodZones`


## Rebuilding the Database
1. update the `scag_dm_init.py` file to match your local source database table
    - in the `else` statement of the `ScagDmInitFixture` class's `import_database` method,
     update the database information to match your local database with the new layer
    - example:

            class ScagDmInitFixture(InitFixture):
                client = 'scag_dm'

                def import_database(self):
                    ...
                    else:
                        return dict(
                            host='localhost', # update
                            database='scag', # the
                            user='example', # info
                            password='example' # here
                        )
                ...

2. run the following command to update the UrbanFootprint database

        time ./manage.py footprint_init --traceback --settings=footprint.settings_init --skip --db_entity --import --layer --tilestache

