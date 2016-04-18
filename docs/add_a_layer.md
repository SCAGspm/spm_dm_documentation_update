# How to add a Global Reference layer
###There are 3 main components of adding a layer:

1. back end code
2. front end code
3. rebuilding the environment

In the below steps, we will walk through how to add an example layer: 'Flood Zones'

## Back End

1. prep your source data table for import
    - name your source data table `scag_<name_of_reference_table>`
        - source table names must start with the word `scag_` as defined in the
         `scag_dm_config_entities.py` file's  `ScagDmConfigEntitiesFixture` class's `regions` method `key='scag'`
        - i.e. tablename = `scag_flood_zones`
2. create the unique db entity key
    - in the `scag_dm_config_entities.py` file's `ScagDmDbEntityKey` class, add the unique key
        - i.e. `FLOOD_ZONES = 'flood_zones'`
        - this lowercase `'flood_zones'` must match the
         `<name_of_reference_table>` from your source data table
        - `FLOOD_ZONES` must be a unique key
3. create the django model class
    - in the `urbanfootprint/footprint/client/configuration/scag_dm/base` directory, create a new python file:
     `<name_of_reference_table>.py`
    - import models and Feature at the beginning of the file (as seen below)
    - name your class the camelcased version of `<name_of_reference_table>` i.e. `FloodZones`
    - match the attributes from your source data table that you would like to see in UrbanFootprint i.e. `fld_zone`
        - django model field type documentation: https://django-document-tchinese.readthedocs.org/en/latest/ref/models/fields.html#field-types
    - add the Meta class within the main feature class
    - `flood_zones.py`

            from django.contrib.gis.db import models

            from footprint.main.models.geospatial.feature import Feature

            __author__ = 'calthorpe_associates'

            class FloodZones(Feature):
                fld_zone = models.CharField(max_length=50, null=True)

                class Meta(object):
                    abstract = True
                    app_label = 'main'

4. create the dbentity in `scag_dm_region.py`
    - add the import statement at the top of the file
        - i.e. `from footprint.client.configuration.scag_dm.base.flood_zones import FloodZones`
    - define the dbentity in the `ScagDmRegionFixture` class's `default_db_entities` method's return statement's `FixtureList`
        - i.e. for `flood_zones`

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

5. define the default style for the layer in `scag_dm_layer.py`
    - in the `ScagDmLayerConfigurationFixtures` class's `layers` method's return statement's `FixtureList`
    add the `LayerConfiguration` for the new layer
    - the following table illustrates the different ways to style a layer based on the type of data: polygon, line, point
    - i.e. for `flood_zones`

            LayerConfiguration(
                library_keys=[LayerLibraryKey.APPLICATION],
                db_entity_key=ScagDmDbEntityKey.FLOOD_ZONES,
                layer_style=dict(

                    geometry_type=GeometryTypeKey.POLYGON,
                    style_attributes=[
                        dict(
                            attribute='fld_zone',
                            style_type=StyleTypeKey.CATEGORICAL,
                            style_value_contexts=[
                                StyleValueContext(value='100 Year Flood Hazard', symbol='=', style=Style(
                                    polygon_fill='#885ead',
                                    line_color='#d3d3d3',
                                    line_width=1,
                                    line_opacity=0.8
                                )),
                                StyleValueContext(value='500 Year Flood Hazard', symbol='=', style=Style(
                                    polygon_fill='#7cb0df',
                                    line_color='#d3d3d3',
                                    line_width=1,
                                    line_opacity=0.8
                                ))
                            ]
                        )
                    ])
            ),


## Front End
 - add to the sproutcore model at `scag_dm_feature_models.js`
    - this should match the django model class
 - add to the sproutcore controller at `scag_delegate.js`
 - add the sproutcore editor view (ie scag_general_plan_parcels_editor_view.js)


## Rebuilding the Environment
- update the `scag_dm_init.py` file to match your local source database table
