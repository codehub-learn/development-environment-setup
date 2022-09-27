# Setting up your environment with Oracle Database and Oracle Data Integrator

## Downloading and Installing Oracle Database

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

## Downloading and Installing Oracle Data Integrator

ODI can be downloaded for free for non-commerical use from 
https://www.oracle.com/middleware/technologies/data-integrator-downloads.html

ODI requires Java SE Development Kit (JDK) version 8u202. It can be downloded from:
https://www.oracle.com/java/technologies/javase/javase8-archive-downloads.html

*Note that using JDK 8u333 may lead to ODI Studio failing to execute. Using JDK version 9 or later is not supported by ODI*

The ODI installer comes in an executable JAR file which requires JDK 8 to run (fmw_12.2.1.4.0_odi.jar). There may be multiple JDKs installed in your system. 
To ensure that the correct one is used without changing your system configuration copy the ODI install JAR to the location of your JDK 8u202 install (e.g. C:\jdk1.8.0_202\bin)
Then, proceed to use the local Java executable to run the installer by opening an (administrator elevated) terminal in the location and running the command *./java.exe -jar fmw_12.2.1.4.0_odi.jar*

## Creating the Oracle Fusion Middleware and ODI Repository

ODI requires the creation of a repository (collection of schemas/tables) in your Oracle Database. The repository is created using the *Fusion Middleware Repository Creation Utility (RCU)*
RCU is an executable bat file (for Windows) or SH (for Unix-based systems) file that can be found in *ORACLE_HOME/oracle_common/bin/rcu_internal.bat*
In the wizard:
 1. Select *System Load and Product Load*
 2. Input the connection details for your Oracle database
 3. In Select Components, ensure that *Master and Work Repositry* under *Oracle Data Integrator* is selected, along with the mandatory *Common Infrastructure Services* component.
 4. In Custom Variables select the default options, like as follows:
![settings snapshot](https://github.com/codehub-learn/development-environment-setup/blob/main/images/RCU_2.png?raw=true)
 5. Make sure to note selected passwords.
 6. Complete the repository creation.
 7. Run ODI Studio from *ODI_INTALL_LOCATION\odi\studio\odi.exe*
 
 
