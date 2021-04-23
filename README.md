Welcome to DataGeol documentation !
================================
> A. Mercier, P.H. Leloup and T. Courrier

_DataGeol_ is a database that allows to organize, store and use geological data efficiently. Upon returning from a field mission, the user can enter the information he has noted in his field notebook in different dedicated tables (measurements, observations, samples, etc.). The different tables are organized and linked together, allowing data to be exported in different formats for processing or display.							
							
The data are organized into several **tables**. Each row is called a **record** and each column a **field**. The field is a single item information that describes the content of the column.
The benefits of storage data into a database : 

* Divides the information into subject-based tables. 
* Provides access to the information as needed, by joining the different tables data. 
* Support and ensure the accuracy and integrity of your information.
* Accommodates your data processing and reporting : needed outputs. 

Getting started
----------------

DataGeol can be run either on Mac, Windows or Linux environment while it has the Microsoft excel installed. The current version of DataGeol has be tested and designed on Excel 2018 64b. 

The database is split in several tables : blue, green or red. 

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

Tables
------
#### LEXICON

This table describes the lexicons used in the database, when a field has an " * ", it means that the column has to be field with a specific lexicon. 

#### MISSIONS

| Column               | Description                                                                             |
|:---------------------|:----------------------------------------------------------------------------------------|
| ID Mission           | Short name describing the field mission. This name will be called by other columns      |
| Detailed name       | Longer name, describing precisely the mission 						 |
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

	       		     								
#### NOTEBOOK

Contact
--------

If you have any questions, comments,  remarks or suggestions, please let us know : 

- Author:	Antoine Mercier
- Contact:	antoine.mercier@univ-lyon1.fr
- version:	4.0

![UniversiteLyon](assets/UDL.png)
