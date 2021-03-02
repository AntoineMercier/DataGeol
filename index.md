---
classes: wide
---

DataGeol documentation
======================
> Antoine Mercier, Philippe Hervé Leloup et Thomas Courrier

DataGeol is a database that allows to organize, store and use geological data efficiently. Upon returning from a field mission, the user can enter the information he has noted in his field notebook in different dedicated tables (measurements, observations, samples, etc.). The different tables are organized and linked together, allowing data to be exported in different formats for processing or display.

Organisation/structure of the database
--------------------------------------

```
├── DataGeol
|   ├── STATIONS.csv               # Table containing the informations about the stations of observations.
|   ├── MEASURES.csv               # Table containing the measures effectuated in the field.
|   ├── CONTACTS.csv         	   # Table containing the contacts between formations (passage points)
|   ├── SAMPLES.csv         	   # Table containing the samples.
|   └── LEXICONS                   # Folder organising the lexicons
|      ├── lexicon_contacts.csv        # Lexicon defining the contacts types
|      ├── lexicon_lines.csv           # Lexicon defining the lines types
|      ├── lexicon_outcrops.csv        # Lexicon defining the outcrops types
|      ├── lexicon_planes.csv          # Lexicon defining the planes types
|      ├── lexicon_samples.csv         # Lexicon defining the samples types
|      └── lexicon_sens-criteria.csv   # Lexicon defining the sens criteria types
	└── AUXILIARY            		# Folder organising auxiliary data
|   	├── Geologists.csv          # Table containing the geologists names and notebooks
|   	├── Missions.csv            # Table containing the missions names and participants
└   	└── stratigraphic_pile.csv  # Table containing the stratigrapic pile
```

Database basics
----------------

The data are organized into several **tables**. Each row is called a **record** and each column a **field**. The field is a single intem information that describes the content of the column.
The benefits of storage data into a database : 

* Divides the information into subject-based tables. 
* Provides acces to the information as needed, by joining the different tables data. 
* Support and ensure the accuracy and integrity of your information.
* Accomodates your data processing and reporting : needed ouputs. 

Getting started
---------------

1. First you must set up your database by organising the AUXILIARY tables : 
	- Define the geologists of your group in the *geologist* table.
	- Define the name of the mission your are doing in the *missions* table.
	- Define the stratigraphic pile you will use in the *stratigraphic_pile* table. Note that you can complete this table later if you don't know yet the pile. 

2. Be aware of the lexicons ! Go through the lexicon tables to know for what are made lexicons. 

3. Fill the database with your observations: 
	1. **STATIONS** : Always start by the *stations* tables. All the other informations will be referenced to this table. 
	2. **MEASURES** : fill the *measures* table with you measure - **every** measure must be associated with a station. 
	3. **CONTACTS** : fill the *contacts* table with the contacts you have observed - **every** sample must be associated with a station. 
	4. **SAMPLES** : fill the *samples* table with you samples - **every** sample must be associated with a station. 

Note : **The fields starting with a " * " indicate that column must be filed by an information defined in a lexicon or an auxiliary table**

Data types
---------

The type of data used is defined for each field : field[DATA TYPE]
You **MUST** ensure to insert the correct data type in each field.

- [VARCHAR] : Character varying, length limited to 45.
- [REAL] : Any real number (ex: 45.86569).
- [INT] : Any integer number (ex: 45).
- [TIME] : Time format yyyy-mm-ddThh:mm:ssZ (given by the GPS).
- [TEXT] : Character varying unlimited length

Consistency of the tables and relationship (if the database is used in PGadmin)
------------------------------------------

**Primary key - tables consistency**
The first column of each table is controlled by the primary key, which maintain the unicity of each row in the table. For example : the row describing the stations of the table *station* must be unique. 

**Foreing key - tables relationship**
The foreing key are links between tables. They maintain the referencial integrity between tables. 
For example : a measure from the table 'measures' is linked to an existing station. The key checks that the station linked to the measure does exist. 

Schema of the database
----------------------

![DataGeol Schema](DataGeol.png "DataGeol")

Contact
----------

If you have any questions, comments,  remarks or suggestions, please let us know : 

- Author:	Antoine Mercier, Philippe Hervé Leloup. 
- Contact:	antoine.mercier@univ-lyon1.fr, philippe-herve.leloup@univ-lyon1.fr
- version:	1.0
