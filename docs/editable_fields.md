## **Appendix B - Fields Descriptions**

#### **Table B1: Editable Layers List with Fields Descriptions**
 *(_Editable Fields are highlighted in Bold Font_ |
 _Data types ~ N: Numeric, S: String_)*

|	Layer	|	Field Name	|	Description	| Type |
|	--------------------	|	--------------------	|	--------------------	| --------------------	|
|	2016 SCAG Entitlement Parcels	|	id	|	System Generated ID	|	N	|
|		|	scaguid16	|	2016 SCAG Unique Parcel ID	|	S	|
|		|	apn	|	Assessor’s Parcel Number	|	S	|
|		|	**tract_no**	|	**Census Tract Number**	|	**S**	|
|		|	**dev_agmt**	|	**Development Agreement Number**	|	**S**	|
|		|	**address**	|	**Project Address**	|	**S**	|
|		|	**date_appro**	|	**Date of Approval**	|	**S**	|
|		|	**date_start**	|	**Start Date**	|	**S**	|
|		|	**multi_par**	|	**Multiple Parcels**	|	**N**	|
|		|	**proj_type**	|	**Project Type**	|	**S**	|
|		|	**pop**	|	**Number of Population**	|	**N**	|
|		|	**du_sf**	|	**Number of Single Family Units**	|	**N**	|
|		|	**du_mf**	|	**Number of Multi-Family Units**	|	**N**	|
|		|	**emp**	|	**Number of Employment**	|	**N**	|
|		|	**emp_type**	|	**Type of Employment**	|	**S**	|
|		|	**emp_sqft**	|	**Square Footage of Employment**	|	**N**	|
|		|	**proj_phase**	|	**Phasing of Project**	|	**S**	|
|		|	**time_limit**	|	**Time Limitation on Development Agreement**	|	**S**	|
|		|	**notes**	|	**User Notes**	|	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	2016 SCAG Existing Land Use Parcels	|	id	|	System Generated ID	|	N	|
|		|	scaguid16	|	2016 SCAG Unique Parcel ID	|	S	|
|		|	apn	|	Assessor’s Parcel Number	|	S	|
|		|	**scag_lu 16**	|	**2016 SCAG Land Use Code**	|	**N**	|
|		|	**scag_lu secondary**	|	**2016 SCAG Land Use Code for secondary use**	|	**N**	|
|		|	scag_lu 12	|	2012 SCAG Existing Land Use Code	|	N	|
|		|	acres	|	Parcel Acreage	|	N	|
|		|	city	|	City Name	|	S	|
|		|	county	|	County Name	|	S	|
|		|	**notes**	|	**User Notes**	|	**S**	|
|		|	land_use_definition_id	|	2016 SCAG Land Use Definition	|	S	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	2016 SCAG General Plan Parcels	|	id	|	System Generated ID	|	N	|
|		|	scaguid16	|	2016 SCAG Unique Parcel ID	|	S	|
|		|	apn	|	Assessor’s Parcel Number	|	S	|
|		|	**scag_gp_code16**	|	**2016 SCAG Land Use Code**	|	**N**	|
|		|	**scag_gp_secondary**	|	**2016 SCAG Land Use Code for secondary use**	|	**N**	|
|		|	scag_gp_code12	|	2012 SCAG General Plan Land Use Code	|	N	|
|		|	**city_gp_code16**	|	**2016 City General Plan Land Use Code**	|	**S**	|
|		|	city_gp_code12	|	2012 City General Plan Land Use Code	|	S	|
|		|	**density**	|	**General Plan Densities: Density**	|	**N**	|
|		|	**low**	|	**General Plan Densities: Lower End**	|	**N**	|
|		|	**high**	|	**General Plan Densities: Higher End**	|	**N**	|
|		|	**year_adopt**	|	**Year Adopted**	|	**S**	|
|		|	acres	|	Parcel Acreage	|	N	|
|		|	city	|	City Name	|	S	|
|		|	county	|	County Name	|	S	|
|		|	**notes**	|	**User Notes**	|	**S**	|
|		|	land_use_definition_id	|	2016 SCAG Land Use Definition	|	S	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	2016 SCAG Infill Parcels	|	id	|	System Generated ID	|	N	|
|		|	scaguid16	|	2016 SCAG Unique Parcel ID	|	S	|
|		|	apn	|	Assessor’s Parcel Number	|	S	|
|		|	**inf_index**	|	**Infill Options: Vacant/Refill**	|	**S**	|
|		|	city	|	City Name	|	S	|
|		|	county	|	County Name	|	S	|
|		|	**notes**	|	**User Notes**	|	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	2016 SCAG Specific Plan Parcels	|	id	|	System Generated ID	|	N	|
|		|	scaguid16	|	2016 SCAG Unique Parcel ID	|	S	|
|		|	apn	|	Assessor’s Parcel Number	|	S	|
|		|	**scag_sp_code16**	|	**2016 SCAG Specific Plan Code**	|	**N**	|
|		|	**scag_sp_secondary**	|	**2016 SCAG Specific Plan Code for secondary use**	|	**N**	|
|		|	**sp_name**	|	**Specific Plan Name**	|	**S**	|
|		|	**city_sp_code16**	|	**2016 City Specific Plan Land Use Code**	|	**S**	|
|		|	**density**	|	**Specific Plan Densities: Density**	|	**N**	|
|		|	**low**	|	**Specific Plan Densities: Lower End**	|	**N**	|
|		|	**high**	|	**Specific Plan Densities: Higher End**	|	**N**	|
|		|	**year_adopt**	|	**Year Adopted**	|	**S**	|
|		|	acres	|	Parcel Acreage	|	N	|
|		|	city	|	City Name	|	S	|
|		|	county	|	County Name	|	S	|
|		|	**notes**	|	**User Notes**	|	**S**	|
|		|	land_use_definition_id	|	2016 SCAG Land Use Definition	|	S	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	2016 SCAG Zoning Parcels	|	id	|	System Generated ID	|	N	|
|		|	scaguid16	|	2016 SCAG Unique Parcel ID	|	S	|
|		|	apn	|	Assessor’s Parcel Number	|	S	|
|		|	**scag_zn_code16**	|	**2016 SCAG Zoning Code**	|	**N**	|
|		|	**city_zn_code16**	|	**2016 City Zoning Code**	|	**S**	|
|		|	city_zn_code12	|	2012 City Zoning Code	|	S	|
|		|	acres	|	Parcel Acreage	|	N	|
|		|	city	|	City Name	|	S	|
|		|	county	|	County Name	|	S	|
|		|	**notes**	|	**User Notes**	|	**S**	|
|		|	land_use_definition_id	|	2016 SCAG Land Use Definition	|	S	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	City/Tier2 TAZ	|	id	|	System Generated ID	|	N	|
|		|	**tier2**	|	**TAZ's Unique ID**	|	**S**	|
|		|	city	|	City Name	|	S	|
|		|	county	|	County Name	|	S	|
|		|	**pop16**	|	**2016 Population**	|	**N**	|
|		|	**pop20**	|	**2020 Population**	|	**N**	|
|		|	**pop35**	|	**2035 Population**	|	**N**	|
|		|	**pop45**	|	**2045 Population**	|	**N**	|
|		|	**hh16**	|	**2016 Households**	|	**N**	|
|		|	**hh20**	|	**2020 Households**	|	**N**	|
|		|	**hh35**	|	**2035 Households**	|	**N**	|
|		|	**hh45**	|	**2045 Households**	|	**N**	|
|		|	**emp16**	|	**2016 Employment**	|	**N**	|
|		|	**emp20**	|	**2020 Employment**	|	**N**	|
|		|	**emp35**	|	**2035 Employment**	|	**N**	|
|		|	**emp45**	|	**2045 Employment**	|	**N**	|
|		|	**notes**	|	**User Notes**	|	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	City Boundary	|	id	|	System Generated ID	|	N	|
|		|	city	|	City Name	|	S	|
|		|	county	|	County Name	|	S	|
|		|	**pop16**	|	**2016 Population**	|	**N**	|
|		|	**pop20**	|	**2020 Population**	|	**N**	|
|		|	**pop30**	|	**2030 Population**	|	**N**	|
|		|	**pop35**	|	**2035 Population**	|	**N**	|
|		|	**pop45**	|	**2045 Population**	|	**N**	|
|		|	**hh16**	|	**2016 Households**	|	**N**	|
|		|	**hh20**	|	**2020 Households**	|	**N**	|
|		|	**hh30**	|	**2030 Households**	|	**N**	|
|		|	**hh35**	|	**2035 Households**	|	**N**	|
|		|	**hh45**	|	**2045 Households**	|	**N**	|
|		|	**emp16**	|	**2016 Employment**	|	**N**	|
|		|	**emp20**	|	**2020 Employment**	|	**N**	|
|		|	**emp30**	|	**2030 Employment**	|	**N**	|
|		|	**emp35**	|	**2035 Employment**	|	**N**	|
|		|	**emp45**	|	**2045 Employment**	|	**N**	|
|		|	acres	|	Acreage	|	N	|
|		|	year	|	Year of Boundary |	N	|
|		|	**notes**	|	**User Notes**	|	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|

#### **Table B2: Reference Layers List with Fields Descriptions**
*(_Editable Fields are highlighted in Bold Font_ |
_Data types ~ N: Numeric, S: String_)*

|	Layer	|	Field Name	|	Description	| Type	|
|	--------------------	|	--------------------	|	--------------------	| --------------------	|
|	2040 High Quality Transit Area/ High Quality Transit Corridors/ Major Transit Stops	|	id	|	System Generated ID	|	N	|
|		|	**notes**	|	**User Notes**	|	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	Transit Priority Area	|	id	|	System Generated ID	|	N	|
|		|	name	|	0.5 Mile Buffer of Major Transit Stop	|	S	|
|		|	county	|	County Name	|	S	|
|		|	**notes**	|	**User Notes**	|	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	Bike Lanes	|	id	|	System Generated ID	|	N	|
|		|	name	|	Name of the Bike Lanes	|	S	|
|		|	status	|	Current Status of the Bike Lanes : Existing; Proposed/Planned, |	S	|
|		|	bike_class	|	Type of Bike Lanes: 1,2,3,4	|	N	|
|		|	length	|	Length of Bike lanes (miles)	|	N	|
|		|	city	|	City Name	|	S	|
|		|	county	|	County Name	|	S	|
|		|	**notes**	|	**User Notes**	|	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	Census Tract	|	id	|	System Generated ID	|	N	|
|		|	geoid10	|	Census Tract ID	|	S	|
|		|	county	|	County Name	|	S	|
|		|	**notes**	|	**User Notes**	|	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	County Boundary	|	id	|	System Generated ID	|	N	|
|		|	county	|	County Name	|	S	|
|		|	acres |	Acreage	|	N	|
|		|	year	|	Year of Boundary | N |
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	California Protected Area Database (CPAD) Holding	|	id	|	System Generated ID	|	N	|
|		|	agency_name	|	Full name of owning agency	|	S	|
|		|	county	|	County Name	|	S	|
|		|	agency_lev	|	Jurisdiction level of agency	|	S	|
|		|	mng_agency	|	Name of agency	|	S	|
|		|	own_type	|	Type of ownership	|	S	|
|		|	site_name	|	Site Name	|	S	|
|		|	city	|	City Holding is within	|	S	|
|		|	desg_agency	|	Designation agency	|	S	|
|		|	desg_nat	|	Primary land management description or designation based on the USGS GAP’s Master Stewardship List (MSL)	|	S	|
|		|	layer	|	Symbology layer: Agency classifications used for general symbology |	S	|
|		|	layer_scag	|	Layer SCAG |	S	|
|		|	scag_acres	|	Scag Areas in Acreas |	N	|
|		|	**notes**	|	**User Notes** |	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	Endangered Species	|	id	|	System Generated ID	|	N	|
|		|	sname	|	Scientific name of a plant or animal	|	S	|
|		|	cname	|	Common name of an element	|	S	|
|		|	elmcode	|	Element code by the Nature Conservancy (TNC)	|	S	|
|		|	occnumber	|	Element occurrence number that identifies a particular instance of a species or community	|	N	|
|		|	kquadname	|	Key quad name	|	S	|
|		|	keycounty	|	Key county	|	S	|
|		|	accuracy	|	Accuracy represents spatial uncertainty in a relative way on a scale of one to ten	|	S	|
|		|	presence	|	Presence refers to the condition of the occurrence at the site when it was last observed	|	S	|
|		|	occtype	|	Occurency type	|	S	|
|		|	fedlist	|	Federal listing status	|	S	|
|		|	callist	|	California State listing status	|	S	|
|		|	location	|	General location of the occurrence	|	S	|
|		|	locdetails	|	Detailed locational information |	S	|
|		|	ecological |	Information relevant to the ecological aspects of the site of the occurrence	|	S	|
|		|	threat	|	Threats present at the site of the occurrence	|	S	|
|		|	general	|	Information about population sizes, site quality, etc. |	S	|
|		|	**notes**	|	**User Notes** |	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	Farmland	|	id	|	System Generated ID	|	N	|
|		|	**scag_type**	|	**SCAG Type**	|	**S**	|
|		|	**fmmp_type**	|	**Farmland Type**	|	**S**	|
|		|	county	|	County Name	|	S	|
|		|	acres	|	Acreage	|	N	|
|		|	year |	Year of Boundary | N	|
|		|	**notes**	|	**User Notes** |	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	Flood Zones	|	id	|	System Generated ID	|	N	|
|		|	scag_fld_zone	|	Flood Zone	|	S	|
|		|	**notes**	|	**User Notes** |	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	Habitat Conservation Areas	|	id	|	System Generated ID	|	N	|
|		|	name	|	Name of the Plan	|	S	|
|		|	type	|	Type of the Plan:	Habitat Conservation Plan (hcp) and Natural Community Conservation Plan (nccp) |	S	|
|		|	stage	|	In what stage is the planning process |	S	|  
|		|	acres	|	Acreage	|	N	|
|		|	**notes**	|	**User Notes** |	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	Scenario Planning Zones |	id	|	System Generated ID	|	N	|
|		|	spzid	|	Scenario Planning Zone ID |	S	|
|		|	county	|	County Name	|	S	|
|		|	city	|	City Name	|	S	|
|		|	**notes**	|	**User Notes** |	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	Sea Level Rise	|	id	|	System Generated ID	|	N	|
|		|	year	|	Year of Boundary |	N	|
|		|	**notes**	|	**User Notes** |	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	Sphere of Influence 	|	id	|	System Generated ID	|	N	|
|		|	soi_name	|	Sphere of Influence |	S	|
|		|	county	|	County Name	|	S	|
|		|	acres	|	Acreage	|	N	|
|		|	year	|	Year of Boundary | N	|
|		|	**notes**	|	**User Notes** |	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
|	Sub Region |	id	|	System Generated ID	|	N	|
|		|	subregion	|	Subregion |	S	|
|		|	name	|	Name |	S	|
|		|	county	|	County Name	|	S	|
|		|	acres	|	Acreage	|	N	|
|		|	year	|	Year of Boundary | N	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
| Truck Routes |	id	|	System Generated ID	|	N	|
|		|	name	|	Name of the Truck Route |	S	|
|		|	city	|	City Name	|	S	|
|		|	county	|	County Name	|	S	|
|		|	**notes**	|	**User Notes** |	**S**	|
|		|	updater_id	|	Username of the User Last Updated	|	S	|
|		|	updated	|	Last Updated Time and Date	|	S	|
|		|	comment	|	System Comment	|	S	|
|		|	approval_status	|	Approval Status (pending/approved/rejected)	|	S	|
