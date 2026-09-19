# Starter Kit and Resources for Data Engineering

## Required Setup

1. [Microsoft SQL Server Developer Edition](#1-microsoft-sql-server-developer-edition)
2. [SQL Server Management Studio](#2-sql-server-management-studio)
3. [AdventureWorks Databases](#3-adventureworks-databases)
4. [Visual Studio Community](#4-visual-studio-community)
5. [SQL Server Development Tools](#5-sql-server-development-tools)
6. [Development IDE](#6-development-ide)
7. [Python](#7-python)
8. [Docker Desktop](#8-docker-desktop)
9. [Power BI](#9-power-bi)
10. [Other Tools](#10-other-tools)

## 1. Microsoft SQL Server Developer Edition

For Windows, download the latest version of **[MSSQL Server Developer edition](https://www.microsoft.com/en-gb/sql-server/sql-server-downloads)**. This is free software and requires no registration.

Execute the SQL20XX-SSEI-Dev.exe, choose Download Media at a specified location 

Use ISO packaging, mount and install 

After checking your computer, select _Custom Installation_ and ensure that _Database Engine, Integration Services, Analysis Services_ are all selected for installation.
Add current user in all cases when prompted.

For authentication, choose *mixed mode authentication* (it may be shown as *SQL Server and Windows Authentication mode*). If you are asked for a user name, use **sa**, and for the password use **passw0rd** (we will only use publicly available sample data for the project so we are ok with basic security) 

## 2. SQL Server Management Studio

For Windows, download the latest version of **[MSSQL Server Management Studio](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15)**. This is free software and requires no registration.

Once it is installed, run it and it will connect to the SQL Server that you installed in the previous step. If it does not auto-connect, select the server from the top tab Browse > Local > (server name).

For authentication, choose *SQL server authentication*, and enter the user name and password which you created in the previous step for the SQL Server. If you get a certificate error, tick the checkbox "Trust Server Certificate" in the connection dialog and connect again.

## 3. AdventureWorks databases

Go to **[this page](https://docs.microsoft.com/en-us/sql/samples/adventureworks-install-configure)** and download the following two databases (they are free to download and use): 

- **[AdventureWorksDW2019.bak](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorksDW2019.bak)**
- **[AdventureWorks2019.bak](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorks2019.bak)**

Be careful with the database names, there are many databases available on that page with similar sounding names. Be sure that you have selected the right ones.

The installation of the databases in MSSQL Server will be shown in one of the course sessions.

## 4. Visual Studio Community
Get **[Visual Studio Community](https://visualstudio.microsoft.com/downloads/)**. Required for the next section.

## 5. SQL Server Development Tools 
1. The **[SQL Server Analysis Services Projects extension](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftAnalysisServicesModelingProjects2022)** installed for Visual Studio. 
2. The **[SQL Server Integration Services Projects extension](https://marketplace.visualstudio.com/items?itemName=SSIS.MicrosoftDataToolsIntegrationServices)** installed for Visual Studio.

As of 22/11/2025, both extensions work for Visual Studio Community 2026. Restart your PC if Analysis extension fails to install. 

## 6. Development IDE 
Get **[Visual Studio Code](https://code.visualstudio.com/download)** for python script execution (do not confuse Visual Studio from #4 with Visual Studio Code).

## 7. Python 
Follow the instructions **[here](https://github.com/codehub-learn/development-environment-setup/blob/main/python-integration-visualization.md)** to download Python. 

## 8. Docker Desktop 
Follow the instructions **[here](https://github.com/codehub-learn/development-environment-setup/blob/main/docker.md)** to download Docker.

## 9. Power BI
Download **[Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/)** and install the PBIDesktopSetup_x64.exe or download it from the **[Windows Store](https://www.microsoft.com/en-us/p/power-bi-desktop/9ntxr16hnw1t#activetab=pivot:overviewtab)**

## 10. Other tools 
1. Git, download and install **[Git Version Control](https://git-scm.com/downloads)**
2. Create a **[Github account](https://github.com/join)**
