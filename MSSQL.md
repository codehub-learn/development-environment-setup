# Starter Kit and Resources for Microsoft SQL Server

## Required Setup

- Microsoft SQL Server Developer Edition
- Microsoft SQL Server Management Studio
- AdventureWorks sample databases

## Microsoft SQL Server Developer Edition

For Windows, download the latest version of [MSSQL Server Developer edition](https://www.microsoft.com/en-gb/sql-server/sql-server-downloads). This is free software and requires no registration.

Execute the SQL2019-SSEI-Dev.exe, choose Download Media at a specified location 

Use ISO packaging, mount and install 

After checking your computer, make full installation, select all options and proceed using default settings 

Add current user in all cases 

For authentication, choose *mixed mode authentication* (it may be shown as *SQL Server and Windows Authentication mode*). If you are asked for a user name, use **sa**, and for the password use **passw0rd** (we will only use publicly available sample data for the project so we are looking for default security) 

## SQL Server Management Studio

For Windows, download the latest version of [MSSQL Server Management Studio](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15). This is free software and requires no registration.

Once it is installed, run it and it will connect to the SQL Server that you installed in the previous step

For authentication, choose *SQL server authentication*, and enter the user name and password which you created in the previous step for the SQL Server

## AdventureWorks databases

Go to [this page](https://docs.microsoft.com/en-us/sql/samples/adventureworks-install-configure) and download the following two databases (they are free to download and use): 

- [AdventureWorksDW2012.bak](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorksDW2012.bak)
- [AdventureWorks2017.bak](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorks2017.bak)

Be careful with the database names, there are many databases available on that page with similar sounding names. Be sure that you have selected the right ones.

The installation of the databases in MSSQL Server will be shown in one of the course sessions.




