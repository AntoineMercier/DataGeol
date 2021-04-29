Welcome to DataGeol documentation !
====================================
> A. Mercier, P.H. Leloup and T. Courrier

_DataGeol_ is a database that allows to organize, store and use geological data efficiently. Upon returning from a field mission, the user can enter the information he has noted in his field notebook in different dedicated tables (measurements, observations, samples, etc.). The different tables are organized and linked together, allowing data to be exported in different formats for processing or display.							
							
The data are organized into several **tables**. Each row is called a **record** and each column a **field**. The field is a single item information that describes the content of the column.
The benefits of storage data into a database : 

* Divides the information into subject-based tables. 
* Provides access to the information as needed, by joining the different tables data. 
* Support and ensure the accuracy and integrity of your information.
* Accommodates your data processing and reporting : needed outputs. 

##### Table of Contents  
* [Getting started](#getting-started)  
* [Database schema](#database-schema)  
* [Tables](#tables)  
* [Export](#export)  
* [Contact](#contact)  

Getting started
----------------

DataGeol can be run either on Mac, Windows or Linux environment while it has the Microsoft excel installed. The current version of DataGeol has be tested and designed on Excel 2018 64b. 

The database is split in several tables : blue, green or red. 

> In order to keep the database consistent, you **must not** change the columns headers. 

| Table color | Description                                                                                             |
|:----------- |:--------------------------------------------------------------------------------------------------------|
| Black       | Lexicon table describing the vocabulary used in the database for geological objects.                    |
| Blue        | Auxiliary tables containing supplementary informations - _to filled by the user_                        |
| Green       | Table containing informations about the location or the observations - _to filled by the user_          |
| Yellow      | Table containing informations about the samples and analysis - _to filled by the user_                  |
| Red         | Output tables generated for GeoModeller or GIS use  - _generated_                                       |

### Data types

Each column filled by the user has a data type description, the user **must** respect the data indicated when filling the column. The type of data used is defined for each field as this : _field[DATA TYPE]_

| Data type   | Description                                             |
|:----------- |:--------------------------------------------------------|
| VARCHAR     | Character varying, any character.			|
| REAL        | Real number (ex: 45.86569).  				|
| INT         | Integer number (ex: 45). 		                |
| TIME        | Time format yyyy-mm-ddThh:mm:ssZ (given by Garmin GPS).	|
| TEXT        | Text characters unlimited length                        |

Database schema
---------------

![DataBaseSchema](assets/schema.png)

Tables
------
#### LEXICON

This table describes the lexicons used in the database, when a field has an " * ", it means that the column has to be field with a specific lexicon. 

#### MISSIONS

| Column               | Description                                                                             |
|:---------------------|:----------------------------------------------------------------------------------------|
| ID Mission           | Short name describing the field mission. This name will be called by other columns      |
| Detailed name        | Longer name, describing precisely the mission 						 |
| Regional plane       | Regional place where the mission took place (ex : South-east of Mont-Blanc massif)      |
| Date                 | Dates of the mission (ex : 01-06-2021 - 15-06-2021)					 |
| Stations             | Range of the stations that have been taken in the field (A1 - A100)			 |
| Participants         | Name of the people that participates to the mission (ex : Antoine Mercier, Hervé Leloup)|
| Field notebook       | Field notebook reference (ex : Alpes1)							 |
| Associated project   | Name of the project associated to the mission (ex : Antoine Mercier PhD)                |

#### MAPS

| Column               | Description                                                                 |
|:---------------------|:----------------------------------------------------------------------------|
| ID Map               | Short name describing the map. This name will be called by other columns    |
| Detailed name        | Longer name, describing precisely the map			             |
| Type                 | Type of the map (geological of topographical)                               |
| Year                 | Year of publication of the map      					     |
| Scale                | Scale of the map : format 1:50 000					     |
| Authors              | Name of the authors that produced the map                                   |


#### LOCATION

| Column                   | Description                                                                                                                                 |
|:-------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| ID Station               | Identification of the station (ex : A1)            					               				                                         |
| Lon [1,2,3]              | Longitude in decimal degree in the WGS84 ellipsoid 					               		                   	                             |
| Lat [1,2,3]              | Latitude in decimal degree in the WGS84 ellipsoid  				 	               				   	                                     |
| Elevation GPS [1,2,3]    | Elevation from the reference ellipsoid measured by GPS in meters   	               						   	                             |
| Elevation baro [1,2,3]   | Elevation from the reference ellipsoid measured by barometer in meters               					  		                             |
| Time [1.2,3]             | Time of the station (format yyyy-mm-ddThh:mm:ssZ)                        		       					   		                             |
| Selected position        | Indicates by a number (1,2 or 3) the position you want to keep as a correct position (default : 1).			           	                 |
| Selected Elevation       | Indicates by a number (1,2 or 3) and a text (baro or GPS) the elevation you want to keep as a correct elevation (ex : 1 baro) (default : 1) |
| Mission                  | Name of the mission (indicated in column _ID Mission_ of the table **_Missions_**) 							                             |
| Outcrop type\*           | Type of the outcrop (described in **_Lexicon_** table)                       		       						                             |
| Direction of observation | Azimuthal direction of the observation (for view point for example) in azimuthal degrees (ex : 265)       					                 |
| Geologist                | Initials or name of the geologist that has taken the station (ex : Antoine Mercier)  							                             |
| Comment                  | Any comment  about the station (ex : along the cliff). 			    								                                     |


Export
------




Contact
--------

If you have any questions, comments, remarks or suggestions, please let us know : 

- Author:	Antoine Mercier, Philippe Hervé Leloup et Thomas Courrier
- Contact:	antoine.mercier@univ-lyon1.fr, philippe-herve.leloup@univ-lyon1.fr, thomas.courrier@ens-lyon.fr
- version:	4.0

![UniversiteLyon](assets/UDL.png)