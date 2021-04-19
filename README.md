![Image alt](https://github.com/YuliaChornenko/db_lab2/blob/main/Logical.png)
![Image alt](https://github.com/YuliaChornenko/db_lab2/blob/main/Physical(1).png)

How to run the script

note: 1st version does not make any sense, this is hello world migration

Install the Spawn https://www.spawn.cc/docs/getting-started.html
Install flyway https://flywaydb.org/documentation/getstarted/firststeps/commandline
Then create data-container by executing the command spawnctl create data-container --image postgres:empty --name flyway-container
Put files from sql folder (github) to flyway's folder sql
Configure flyway.conf accordingly to the data-container credentials
Run ./flyway migrate
If you want to check Data Ingestion processes follow the next workflow:

Run 1-10 version
run main.py script from lab1 with a new credentials (I also strongly recommend ingesting only first 50 rows from Odata2020file.csv to save the time)
Then run 11th and 12th versions
Summary:

Differentiated the table zno_results to person, registration, education, cityregion
The main relations are:
* outid in person 1->n outid in results
* RegistrationLocation person n<-1 locationID in registration
* EOName person 1 -> EOName in education
Created schema migration and data ingestion processes
