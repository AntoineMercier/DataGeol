Welcome to DataGeol documentation !
================================
> A. Mercier, P.H. Leloup and T. Courrier

DataGeol is a database that allows to organize, store and use geological data efficiently. Upon returning from a field mission, the user can enter the information he has noted in his field notebook in different dedicated tables (measurements, observations, samples, etc.). The different tables are organized and linked together, allowing data to be exported in different formats for processing or display.							
							
Database basics
----------------

The data are organized into several **tables**. Each row is called a **record** and each column a **field**. The field is a single intem information that describes the content of the column.
The benefits of storage data into a database : 

* Divides the information into subject-based tables. 
* Provides acces to the information as needed, by joining the different tables data. 
* Support and ensure the accuracy and integrity of your information.
* Accomodates your data processing and reporting : needed ouputs. 

Data types
---------

The type of data used is defined for each field : field[DATA TYPE]
You **MUST** ensure to insert the correct data type in each field.

- [VARCHAR] : Character varying, length limited to 45.
- [REAL] : Any real number (ex: 45.86569).
- [INT] : Any integer number (ex: 45).
- [TIME] : Time format yyyy-mm-ddThh:mm:ssZ (given by the GPS).
- [TEXT] : Character varying unlimited length


LOCATION
--------
You can choose the position and elevation you want to use in the selected position. If no selection indicated, by default the first one will be used. 



Contact
----------

If you have any questions, comments,  remarks or suggestions, please let us know : 

- Author:	Antoine Mercier
- Contact:	antoine.mercier@univ-lyon1.fr
- version:	4.0
