# Setting up your environment with Oracle Database

Oracle Database Enterprise can be installed for free for non-commerical usage. Download and install Oracle Database 21c Enterprise Edition from the following link:
https://www.oracle.com/cis/database/technologies/oracle-database-software-downloads.html

**During installation do be careful to note the selected Pluggable Database (PDB) name and the password selected for the sys user, as they will be required in later steps.**

![db_install_snapshot](https://github.com/codehub-learn/development-environment-setup/blob/main/images/db_5a.png?raw=true)

*Note that a free Oracle account is required to proceed with the download*

Also download and intall the latest version of Oracle SQL Developer, from the following link:
https://www.oracle.com/database/sqldeveloper/technologies/download/

*Note that for Windows users the version with JDK included is reccomended. For uses in Linux or MacOS environments downaloading and installing the specified 
Java Development Kit (JDK) version is required to run Oracle SQL Developer. To download the JDK, refer to the following link: 
https://www.oracle.com/java/technologies/downloads/#java11*

Lastly, download the Oracle *HR* sample database schema and create it in your system. To download and install the schema, follow the below steps:
Download all sample schema files from https://github.com/oracle-samples/db-sample-schemas

1. In hr_main.sql replace all mentions of __SUB__CWD__ with the directory containing your download. For example if you the location of the hr_code.sql file in your computer is C:/OracleSamples/Human Resources/hr_code.sql the line should be changed from @__SUB__CWD__/human_resources/hr_code to @C:/OracleSamples/Human Resources/hr_code
2. If not already started, start your Oracle Database listener with an (administrator) command prompt by entering lsnrctl start (attempting to use this command from a non-administrator terminal may result in an error).
3. Connect to SQL*Plus using sqlplus / as sysdba 
4. Execute the hr_main script by inputting a @ followed by the file location e.g. @C:/OracleSamples/Human Resources/hr_main
5. During script execution: 
    When prompted for the default tablespace enter *Users*
    When prompted for the default temp tablespace enter *Temp*
    When prompted for the sys user password enter your sys (root) Oracle user password
    When prompted to enter the log file location enter a file system location e.g. C:/
    When prompted for the connection string use syntax host:port/service for a pluggable database (e.g. *localhost:1521/orclpdb*)

*For more information also refer to Oracle’s documentation at https://docs.oracle.com/en/database/oracle/oracle-database/21/comsc/installing-sample-schemas.html#GUID-CB945E4C-D08A-4B26-A12D-3D6D688467EA*

