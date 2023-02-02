# Hardware and software requirements for SQL Server Analysis Services (SSAS) 
Getting your workstation ready for SQL Server Analsyis Services (SSAS) project development. 

## Workstation specifications 
- Windows 10 
- RAM, 8GB required, 16GB preferable 
- 128 GB Storage (SSD would be preferrable) 
- 4 Core CPU 

## Development IDE 

**[Visual Studio Community](https://visualstudio.microsoft.com/downloads/)**  or better with the Data storage and processing workload installed, including the SQL Server Data Tools component. 

## SSAS Development Tools 
1. An **[SQL Server Developer Edition](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)**  or better instance **with the Analsysis Services Multidimensional mode component installed.**
2. A (second) **[SQL Server Developer Edition](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)** or better instance **with the Analysis Services Tabular mode component installed.**
3. The **[Microsoft Analysis Services Projects extension](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftAnalysisServicesModelingProjects2022)** installed for Visual Studio. 
4. **[SQL Server Management Studio](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15)** (SSMS) 

Refer to **[Microsoft's Guide](https://learn.microsoft.com/en-us/analysis-services/instances/install-windows/install-analysis-services?view=asallproducts-allversions)** on installing Analysis Services.
Note that Multidimensional and Tabular modes cannot coexist on the same instance. A second installation of SQL Server will be required to maintain both.
