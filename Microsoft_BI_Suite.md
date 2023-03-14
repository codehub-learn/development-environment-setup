# Starter Kit and Resources for Microsoft Business Intelligence Suite

## Required Setup

- Microsoft SQL Server Developer Edition
- Microsoft SQL Server Management Studio
- Analysis Services (SSAS) (SQL Server Component and Visual Studio Extension)
- Integration Services (SSIS) (SQL Server Component and Visual Studio Extension)
- Power BI Desktop
- Visual Studio 2019 Community
- AdventureWorks sample databases

## Microsoft SQL Server Developer Edition

For Windows, download the latest version of **[MSSQL Server Developer edition](https://www.microsoft.com/en-gb/sql-server/sql-server-downloads)**. This is free software and requires no registration.

Execute the SQL2019-SSEI-Dev.exe, choose Download Media at a specified location 

Use ISO packaging, mount and install 

After checking your computer, select _Custom Installation_ and ensure that _Database Engine, Integration Services, Analysis Services_ are all selected for installation.
Add current user in all cases when prompted.

For authentication, choose *mixed mode authentication* (it may be shown as *SQL Server and Windows Authentication mode*). If you are asked for a user name, use **sa**, and for the password use **passw0rd** (we will only use publicly available sample data for the project so we are ok with basic security) 

## SQL Server Management Studio

For Windows, download the latest version of **[MSSQL Server Management Studio](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15)**. This is free software and requires no registration.

Once it is installed, run it and it will connect to the SQL Server that you installed in the previous step

For authentication, choose *SQL server authentication*, and enter the user name and password which you created in the previous step for the SQL Server

## AdventureWorks databases

Go to **[this page](https://docs.microsoft.com/en-us/sql/samples/adventureworks-install-configure)** and download the following two databases (they are free to download and use): 

- **[AdventureWorksDW2019.bak](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorksDW2019.bak)**
- **[AdventureWorks2019.bak](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorks2019.bak)**

Be careful with the database names, there are many databases available on that page with similar sounding names. Be sure that you have selected the right ones.

The installation of the databases in MSSQL Server will be shown in one of the course sessions.

## Development IDE 

**[Visual Studio 2019 Community](https://docs.microsoft.com/en-us/visualstudio/releases/2019/release-notes)**  or better with the Data storage and processing workload installed, including the SQL Server Data Tools component. 

## SQL Server Development Tools 
1. The **[SQL Server Analysis Services Projects extension](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftAnalysisServicesModelingProjects)** installed for Visual Studio. 
2. The **[SQL Server Integration Services Projects extension](https://marketplace.visualstudio.com/items?itemName=SSIS.SqlServerIntegrationServicesProjects)** installed for Visual Studio. 

## Power BI
Download **[Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/)** and install the PBIDesktopSetup_x64.exe or download it from the **[Windows Store](https://www.microsoft.com/en-us/p/power-bi-desktop/9ntxr16hnw1t#activetab=pivot:overviewtab)**

## Other tools 
1. Git, download and install **[Git Version Control](https://git-scm.com/downloads)**
2. Create a **[Github account](https://github.com/join)**
