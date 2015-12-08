![UF Logo](images/uf_logo.png)

![scag_logo](images/scag_12_7_15/scag_logo.png)
![calthorpe_logo](images/scag_12_7_15/calthorpe_logo.png)

# SCAG UrbanFootprint Scenario Planning Model (SPM)

## User Manual for Data Review and Editing

The data review and editing framework within SCAG UrbanFootprint SPM provides the user with a number of data management and data review options. Using attribute query and map selector tools, the user can explore data, summarize attributes, and edit configured layers.  This documentation covers basic SPM functionality for data review and editing. 

## Introduction

SCAG UrbanFootprint-based Scenario Planning Model (SPM) is a land use planning, modeling, and data management tool that is undergoing development to facilitate more informed and collaborative planning by local jurisdictions and other stakeholders. Built on a web-based geospatial platform with full co-benefit analysis capacity, the SPM allows planners to develop future scenarios for land use, transportation infrastructure, and socio-economic growth distribution.

The UrbanFootprint model, an Open Source software product being customized and enhanced for use by California Metropolitan Planning Organizations (MPOs), serves as the platform for the SPM. Currently, SCAG, Sacramento Area Council of Governments (SACOG), and San Diego Association of Governments (SANDAG) are all contributing to the effort to customize UrbanFootprint, and enhancements will be shared by all users and ultimately made available to local jurisdictions across Southern California.

This pilot process is intended to demonstrate how local and regional data can be served to local jurisdictions via the SPM web-based user interface, and to test initial functions focused primarily on data review and editing.  The data review and editing framework within SPM provides the user with a number of data management and data review options. Using attribute query and map selector tools, the user can explore data, summarize attributes, and edit configured layers.  **This documentation covers basic SPM functionality for data review and editing.**

Ultimately, the SPM once completed will bring robust scenario-development functionality to local jurisdictions across the SCAG region.  For more information, please visit our website at http://sp.scag.ca.gov.

**System Requirements**

The SPM is accessed via a web page. Ultimately, any web browser will be able to access the system effectively, as will nearly all desktops, laptops, and tablets. For access to the pilot site, there are some more refined, through fairly minimal, requirements: 

* A relatively recent (purchased in last 5 years) desktop or laptop computer running the Windows, Mac OSX, or Linux operating systems. The current system has not been optimized for tablet or touchscreen operating systems or interfaces. 

* Current version of Google Chrome web browser. Chrome is available via free download at https://www.google.com/intl/en/chrome/browser/

* Mouse, track-ball, or trackpad-based input device (essentially all desktop or laptop computers have this capability). 

> **Note:** If you experience difficulties in performing feature editing (e.g., feature selection, querying, etc.) 
> while being able to view maps on the SPM, first check your internet firewall configuration with the local IT support. 
> The URL of the SPM data management site should be added to the trust list of firewall configuration in order to avoid
> block access by web filters set up locally.

## Data Management Framework - Site Map     

![site_map](images/scag_12_7_15/site_map.png)

## User Interface Overview 

### Layer Management Window 

The Layer Management window on the left side of the SPM user interface displays layers that have been preloaded into the SPM, and that can be turned on for display and activated for selection, editing, and queries.   

The user can select an active layer by clicking on the layer name and the active layer will be highlighted in blue. 

> **Important:** Any map selection, attribute query, export 
> layer, export csv initiated by the user will occur on the 
> active layer regardless of whether it is visible or not.

[layers_icon]: <images/scag_12_7_15/layers.png>
[reorder_arrow]: <images/scag_12_7_15/reorder_arrow.png>
[reorder_layers]: <images/scag_12_7_15/reorder_layers.png>

*Editable Layer*: Any layer under the Editable Layers contains editable fields by the user.

![editable_layers](images/scag_12_7_15/editable_layers.png)

![Layers Button][layers_icon] *Exporting Active Layer*: The user can export the Active Layer to a geodatabase (.gdb) by clicking on the layers button on the Layers Tool Bar. The user can initiate exporting by clicking ‘OK’ on a window that opens up (see Figure 3) once the user clicks on the ‘Export Active Layer – to gdb’ button.  By default, the exported layer is saved to the Windows default Download folder. 

![Reorder Arrow][reorder_arrow] *Reordering Map Layers*: The user can re-order layers on the map by clicking on the arrow button on the right side of the Layers Tool Bar. This button will open a window where the user can order the layers by clicking on the layer name and dragging it into the order the user prefers within the visible list. This order corresponds to the layer order on the map. 

![Re-Order Layers][reorder_layers]

### Map Tool Bar

Clicking on an icon on the map tool bar allows the user to zoom and navigate around the map as well as select and identify map features. The user can hover their pointer to get the ‘tool tip’ to identify what button corresponds with each selector. 

[selector_tools]: <images/scag_12_7_15/selector_tools.png>
![Toolbar][selector_tools]

[extent_selector]: <images/scag_12_7_15/extent_selector.png>
[zoom_selected]: <images/scag_12_7_15/zoom_selected.png>
[cancel_select]: <images/scag_12_7_15/cancel_select.png>
[hand_select]: <images/scag_12_7_15/hand_select.png>
[pointer_select]: <images/scag_12_7_15/pointer_select.png>
[box_select]: <images/scag_12_7_15/box_select.png>
[polygon_select]: <images/scag_12_7_15/polygon_select.png>
[info_select]: <images/scag_12_7_15/info_select.png>

![Zoom to Extent][extent_selector] *Zoom to Project Extent*: This tool allows the user to zoom the current map to the project map extent. The project in the SPM refers to a local jurisdiction or County.
 
![Zoom to Selection][zoom_selected] *Zoom to Selection Extent*: This tool allows the user to zoom the current map to the extent of selected features of the Active Layer.
 
![Clear Selection][cancel_select] *Clear Selection*: This tool clears the selected features of the Active Layer.
 
![Navigate][hand_select] *Navigate*: This tool allows the user to navigate around the map by clicking and dragging on the map. The user can hold ‘Shift’ and drag to create zoom extent.
 
![Point Selector][pointer_select] *Point Selector*: The point selector selects the feature that intersects with a point where the user clicks on the map.
 
![Rectangle Selector][box_select] *Rectangle Selector*: The rectangle selector selects the feature that intersects with a rectangle formed by the user clicking and dragging across the map.
 
![Polygon Selector][polygon_select] *Polygon Selector*: The polygon selector selects the feature that intersects with a user defined polygon shape formed by the user defining each node of the polygon by clicking on the map. Double clicking will stop forming the polygon selection.
  
![Identify][info_select] *Identify*: This tool is activated when a feature is selected. The Identify tool opens a moveable summary window where the user can view the attributes of the selected feature. 



### Top Section Menu Pane

The top section menu drop down allows the user to toggle between Project Info, Data Explorer, and Approval/Merge options. After clicking one of the options, the map selection will resize display the selected option.

![topbar_opening](images/scag_12_7_15/top_bar_closed_to_open.png)

[menu_button]: <images/scag_12_7_15/menu_button.png>
[approval_merge]: <images/scag_12_7_15/approval_icon.png>
[data_explorer]: <images/scag_12_7_15/query.png>
[project_info]: <images/scag_12_7_15/chart_icon.png>

The user can toggle between the following options by clicking on the menu button: 

**Project Info:** The user can switch between Master and Draft Scenarios and see metadata about the active scenario.

**Data Explorer:** The user can define attribute queries and join tables to explore the data.

**Approval/Merge:** The user who has a manager level or director level permission can approve edits and merge those edits into mater versions of the editable layers. 


![Project Info][project_info] ***Project Info***      

**TODO update this, I(janet) just wrote something here as filler**

This screen displays charts on Population, Households, and Employment on the current project.
 
![Data Explorer][data_explorer] ***Data Explorer*** 

The data explorer query functionality and the map selector tools in the SPM are linked by default. When a user selects features on the map with the map selector tools, the attributes will populate in the query window. If the user inputs an attribute query with no map selection, the map will show the features selected from the attribute query. The user also has the option to use attribute selections and map selections in combination.  

**Querying Attributes**: 
>SPM attribute querying functionality utilizes SQL syntax to tell the database what features the user would like to select. The user can select attribute names from a drop down list by clicking on the arrow button next to the ‘Where’ clause or type them in.  

![query_ui](images/scag_12_7_15/query_ui.png)

*The following comparison/equality operators are supported:* 

* Greater than : >
* Less than : <
* Greater than or equal to : >=
* Less than or equal to : <=
* Equals : =
* Not equal: !=

*For querying strings, the following syntax can be used (must be capitals):* 

* BEGINS_WITH : String begins with a certain letter or group of letters
* ENDS_WITH : String ends with a certain letter or group of letters
* CONTAINS: String contains a certain letter or group of letters

*Multiple attribute queries are supported using the following syntax (must be capitals):*

* AND : SQL ‘and’ syntax, attributes must meet both query requirements
* OR : SQL ‘or’ syntax, attributes must meet either query requirements

> **Tip:** User can access a drop down of attributes, operators, and AND/OR/parenthesis syntax for a quicker query.

**Query Examples:**

 **Example 1**

 Returns all rows with land use code 1200 with a dwelling unit count greater than 2:

    land_use12 = 1200 AND du >= 2

 **Example 2**

 Returns all parcels with an apn that begins with 580 or an apn that begins with 104:

    apn BEGINS_WITH "580" OR apn BEGINS_WITH "104"

>Any string query must have quotation marks around values.


**Joining Tables:**

SPM allows the user to seamlessly join and query spatial tables of different geography types and geographic scales. Each layer in the system is tagged with a join type when it is imported. The join types include attribute joins, polygon to polygon, polygon to centroid, and centroid to polygon joins. This processing is handled ‘behind the scenes’ in the system. 
The user utilizes these pre-defined join tables by selecting the desired table from the drop down button in the query window. Having selected a table to join, the user will have access to all fields in that join table. Any query making use of join fields will utilize the pre-defined spatial or attribute relationship. 

>**Important:** If the user is querying a field from the join table that has the same name as a field in the source table, the system defaults to the source table field.
> To query the join table field, the user must write the *name_of_join_table.field_name* or select it from a drop down list by clicking the arrow next to the 'Where' clause in the Query window.



**Query Options:**

The user has a number of options to form their query and to show helpful information in the user interface:

![query_ui_limit_results](images/scag_12_7_15/query_ui_limit_results.png)

* Limit Results to Selected Area: If the user has selected features with a map selector tool and input an attribute query, they have the option to limit the query result to the map selection or apply them to the whole dataset. 
* Show Selection Shape on Map: The user can toggle on and off the map selection shape 
* Clear Button: Clears the selection
* Query Button: Executes the query
* Select Attributes Shortcut: Allows user to select from a drop down of attributes
* Operators Shortcut: Allows user to select operators from a drop down list
* AND/OR shortcut: Allows user a shortcut to the common AND/OR/parenthesis operators



![Approval and Merging][approval_merge] ***Approval/Merging***

The Approval/Merging interface is accessible to users with manager or director level permissions. The approval interface allows data managers to review and approve/reject edits made by any user. Through easy to use drop-down queries, edited features can be reviewed, approved or rejected, and merged into the master version. 

![approval_merge_top_section](images/scag_12_7_15/approval_merge_top_section.png)

**Approving/Rejecting Edits:** 

The approval interface acts on the active layer. When a data manager is ready to approve or reject edits, they can load all pending edited rows (needing approval) by selecting the correct query form the drop down list. If the user would like to review previously approved or rejected features, the system provides those options as well. 

![approval_merge_dropdown](images/scag_12_7_15/approval_merge_dropdown.png)

Once the data has loaded, the user can highlight a given row (or group of rows by holding down CTRL) to see the location on the map. The user can approve or reject the highlighted rows by pushing the corresponding “Approve” and “Reject” buttons. If the user would like to simply approve or reject all edits, toggling ‘Select All’ will highlight all rows. Once highlighted, all rows can then be approved or rejected. Once rows have been approved or rejected, the user must save their edits. Any approval or rejections that are not saved will be ignored. 

![approval_merge_approve_reject_buttons](images/scag_12_7_15/approval_merge_approve_reject_buttons.png)

**Merging:** 

Once features have been reviewed and edits approved, the data manager can merge all approved features into the Master version of the layer. Within the approval interface, the user can toggle the Merge screen. This will provide the user with the option to merge approved features. After clicking on the Merge button, a backend process will handle filtering and merging data tables. 

![approval_merge_merge_button](images/scag_12_7_15/approval_merge_merge_button.png)


### Edit Window

The Edit Window allows the user to edit or comment upon select layer attributes. Currently attribute editing requires custom edit forms to be made specifically for configured layers in SPM; any layer not configured for editing is not editable (see Appendix B for the list of editable layers). If a layer has been configured, when that layer is active in the layer manager, the user can open an edit window by clicking on the ‘Edit’ button on the right side of the screen to view and edit specific attributes. See Figure 14 below. 
The editor operates on the currently selected features of the active layer. If there is more than one feature selected, any changes made in the editor window will populate all rows with those values unless the layer is configured to only allow editing of one row at a time. 


.. |export_csv_button| image:: images/exportcsv.png

Similar to querying syntax, aggregation syntax makes use of the SQL database language. The user has options to aggregate any field in the active table and any field in a table that has been joined. Aggregation includes both aggregation operators and â€˜group byâ€™ results. The user can also decide whether to aggregate within the active map selection or from the entire dataset.

.. figure:: images/aggregation_window.png
    :alt: aggregation window
    :align: right
    
    Figure 8: Aggregation window

*Aggregation Syntax:* The following aggregation operators are active in UrbanFootprint:

- SUM(field_name): Sum of the values of the assigned field.
- COUNT(field_name): Count the number of rows from the assigned field.
- AVG(field_name): Average of the values of the assigned field. 
- MAX(field_name): Maximum value of the assigned field. 
- MIN(field_name): Minimum value of the assigned field. 

Multiple fields can be aggregated at the same time by separating the aggregation functions with commas. An example of this syntax is as follows::

    SUM(field_name), AVG(field_name2), COUNT(field_name3), SUM(field_name4)

*Group By:* UrbanFooptrint allows the user to specify one or more group by fields. â€˜Group Byâ€™ allows the user to summarize fields by categorical variables. A common group by field is a parcel land use code column, but any categorical variable can be used. If a group by column is specified, aggregations will return values for each distinct value in the group by column. 

An example of a group by configuration can be seen in Figure 10 below. In this case, the aggregation is to sum all the employment from the TAZ record by unique TAZ id and to count the number of parcels within each TAZ from the parcel data set. The results are also limited to a painted selection.

.. figure:: images/aggregation_groupby.png
    :alt: aggregation using group by
    :align: right
    
    Figure 9: Aggregation using group by

The user can export the results from a query or summary to a .csv file format by clicking on the |export_csv_button| button in the top right corner of the screen.

Scenario Painting
=================

.. |apply_button| image:: images/apply.png

Scenario painting requires custom edit forms to be made specifically for configured layers in UrbanFootprint, and therefore can only be implemented on layers with the |pencil_icon| icon. When such a layer is active in the layer manager, the user can open an edit window on the right side of the screen to view and change specific attributes. See Figure 10 below:

.. figure:: images/attribute_edit_window.png
    :alt: attribute editing window
    :align: right
    
    Figure 10: Attribute editing window

The user can adjust the development, density, and gross/net percentages using the toggles at the top of the panel. To save changes to edited attributes the user must click on â€˜Applyâ€˜ |apply_button| when finished editing. *If the user changes the selected features without applying changes, those changes will not be saved.* The user can see the effects of these adjustments on the numbers of dwelling units, employees, and acres developable at the bottom of the screen.

Built Form Editor
-----------------

.. |down_arrow| image:: images/down_arrow.png

Click on the down arrow |down_arrow| to manage built forms using the Built Form Editor, which operates on the currently selected features of the active layer. If there is more than one feature selected, any changes made in the editor window will populate all rows with those values. In cases where a layer is configured to only allow editing of one row at a time, the following message will be displayed indicating that only one record at a time can be edited:

.. figure:: images/one_record.png
    :align: center
    
Within the Built Form Editor, the user can edit a building, building type, or placetype. See Figure 11 below:

.. figure:: images/built_form_editor.png
    :align: center
    
    Figure 11: Built Form Editor window

Analysis Modules
----------------

The Water and Energy Modules can be run from the analysis panel on the right side of the screen...