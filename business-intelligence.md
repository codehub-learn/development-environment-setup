# Hardware and software requirements for Business Intelligence
&nbsp;

## PC's specs
- 8 GB RAM
- 128 GB Storage (SSD would be preferrable)
- 4 Core CPU
- Windows 10, 64 bit

## Important notice
Mac or Linux users can install MS-SQL server using Docker. Instead of Management Studio, Azure Portal Application can be used but without the diagrammatic capabilities. Power BI is NOT supported. Windows in a virtual machine can be an option, or dual boot. 

## Required software 
You will need the MS-SQL Server database (RDBMS), the MS-SQL Server management interface and the Power BI desktop application.
In detail you have to download:

1.  [SQL Server Developer 2019 ](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
    - Download the Developer edition (SQL2019-SSEI-Dev.exe)
    - Execute the SQL2019-SSEI-Dev.exe,  choose Download Media at a specified location
	- Use ISO packaging, mount and install
	- After checking your computer, make full installation, select all oprions and proceed using default settings
	- Add current user in all cases
	- Choose mixed mode authentication using the password
        Password: `passw0rd`	

1.  [SQL Server Management Studio, SSMS 18.5.1](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15) 
and install the SSMS-Setup-ENU.exe file.

3. Power BI
**[Download the Power BI Desktop](https://www.microsoft.com/en-us/download/details.aspx?id=58494)**
and install the PBIDesktopSetup_x64.exe.

&nbsp;
&nbsp;

# Demo databases for Business Intelligence

## AdventureWorks download links 

[OLTP version of AdventureWorks](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorks2012.bak)
[DW version of AdventureWorks](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorksDW2012.bak)

## Restore instructions
Follow the below steps to restore a backup of your database using SQL Server Management Studio.

1. Open SQL Server Management Studio and connect to the target SQL Server instance.
2. Right-click on the Databases node, and select Restore Database.
3. Select Device and click the ellipses (...)
4. In the dialog Select backup devices, click Add, navigate to the database backup in the filesystem of the server, and select the backup. Click OK.
5. If needed, change the target location for the data and log files, in the Files pane. Note that it is best practice to place data and log files on different drives.
6. Click OK. This will initiate the database restore. After it completes, you will have the AdventureWorks database installed on your SQL Server instance.
