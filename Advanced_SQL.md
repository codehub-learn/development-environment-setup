# Starter Kit and Resources for Microsoft SQL Server

## Required Setup

- Microsoft SQL Server Developer Edition
- Microsoft SQL Server Management Studio
- AdventureWorks sample databases

## Microsoft SQL Server Developer Edition

For Windows, download the latest version of [MSSQL Server Developer edition](https://www.microsoft.com/en-gb/sql-server/sql-server-downloads) from the webpage section "free specialized edition". This is software free to use for non-production work and requires no registration.

Execute the SQL2022-SSEI-Dev.exe, choose Express Installation

## SQL Server Management Studio

For Windows, download the latest version of [MSSQL Server Management Studio](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16). This is software free to use and requires no registration.

Once it is installed, run it and it will connect to the SQL Server that you installed in the previous step

For authentication, choose *SQL server authentication*, and enter the user name and password which you created in the previous step for the SQL Server

## AdventureWorks databases

Go to [this page](https://docs.microsoft.com/en-us/sql/samples/adventureworks-install-configure) and download the following two databases (they are free to download and use): 

- [AdventureWorksDW2022.bak](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorksDW2022.bak)
- [AdventureWorks2022.bak](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorks2022.bak)

Be careful with the database names, there are many databases available on that page with similar looking names. Be sure that you have selected the right ones.

The installation of the databases in MSSQL Server will be shown in one of the course sessions.
