# Starter Kit and Resources for SQL Server Reporting Services (SSRS)

## Required Setup

- Microsoft SQL Server Developer Edition or Better
- Microsoft SQL Server Management Studio
- Visual Studio Community or Better with Reporting Services Projects Extension
- AdventureWorks and WideWorldImporters Sample Databases

## Microsoft SQL Server Developer Edition

For Windows, download the latest version of [MSSQL Server Developer edition](https://www.microsoft.com/en-gb/sql-server/sql-server-downloads). This is free software and requires no registration.

Execute the SQL20XX-SSEI-Dev.exe, choose Download Media at a specified location 

Use ISO packaging, mount and install 

After checking your computer, select _Custom Installation_ and ensure that _Database Engine, Integration Services, Analysis Services_ are all selected for installation.
Add current user in all cases when prompted.

For authentication, choose *mixed mode authentication* (it may be shown as *SQL Server and Windows Authentication mode*). If you are asked for a user name, use **sa**, and for the password use **passw0rd** (we will only use publicly available sample data for the project so we are ok with basic security) 

## SQL Server Management Studio

For Windows, download the latest version of [MSSQL Server Management Studio](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15). This is free software and requires no registration.

Once it is installed, run it and it will connect to the SQL Server that you installed in the previous step

For authentication, choose *SQL server authentication*, and enter the user name and password which you created in the previous step for the SQL Server

## Sample databases

- [AdventureWorksDW2019.bak](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorksDW2019.bak)
- [AdventureWorks2019.bak](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorks2019.bak)
- [WideWorldImporters.bak](https://github.com/Microsoft/sql-server-samples/releases/download/wide-world-importers-v1.0/WideWorldImporters-Full.bak)
- [WideWorldImportersDW.bak](https://github.com/Microsoft/sql-server-samples/releases/download/wide-world-importers-v1.0/WideWorldImportersDW-Full.bak)

The installation of the databases in SQL Server will be shown in one of the course sessions.

## Development IDE 

**[Visual Studio 2022 Community](https://visualstudio.microsoft.com/vs/community/)**  or better with the Data storage and processing workload installed, including the SQL Server Data Tools component. 

## SQL Server Development Tools 
The **[SQL Server Reporting Services Projects](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftReportProjectsforVisualStudio2022)** installed for Visual Studio. 
