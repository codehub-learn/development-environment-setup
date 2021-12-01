# Getting your computer ready for Fintech Development

### Workstation specifications
- Windows 10 or Linux or MacOS, 64 bit
- RAM, 8GB required, 16GB preferable
- 128 GB Storage (SSD would be preferrable)
- 4 Core CPU

### Accounts
1. Email account
2. **[Github account](https://github.com/join)**


## Java with Spring Framework

### Development IDE
**[Download IntelliJ IDEA Ultimate](https://www.jetbrains.com/idea/download/#section=windows)** and install. In case you already have it installed and your license has expired, we will provide you a valid license for the duration of the course. In case you prefer using another IDE, that's also fine as the examples do not make use of any IDE specific functionality. 

### Java Development Tools
1. Java Development Toolkit, download and install the **[JDK 11](https://adoptium.net/)**. Create then an environmental variable named **JAVA_HOME** pointing to JDK installation folder.
2. Maven, download **[Maven](https://maven.apache.org/download.cgi)** and follow the **[instructions](https://maven.apache.org/install.html)**. Through Maven dependency management mechanism, we will download every library needed in our projects.  Create then an environmental variable named **MVN_HOME** pointing to Maven's installation folder.
3. Add **%JAVA_HOME%/bin** and **%MVN_HOME%/bin** to your **PATH** envrionmental variable.

### Database development tools
1. **[SQL Server Developer 2019](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)**.
    -	Download the Developer edition (SQL2019-SSEI-Dev.exe).
    -	Execute the SQL2019-SSEI-Dev.exe, choose Download Media at a specified location.
    -	Use ISO packaging, mount and install.
    -	After checking your computer, make full installation, select all options and proceed using default settings.
    -	Add current user in all cases.
    -	Choose mixed mode authentication. If you are asked for a password, use **passw0rd** (we will only use publicly available sample data for the project so we are looking for default security)
2. **[SQL Server Management Studio](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms)**, SSMS and install the SSMS-Setup-ENU.exe file.

### Other tools
1. Download and install **[Git Version Control](https://git-scm.com/downloads)**.
2. Install **[Postman Client](https://www.postman.com/downloads/)**.

## Power BI
Download the **[Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/)** and install the PBIDesktopSetup_x64.exe.

### Demo databases for Business Intelligence
**[OLTP version of AdventureWorks](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorks2012.bak)**, **[DW version of AdventureWorks](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorksDW2012.bak)**

### Database restore instructions
Follow the below steps to restore a backup of your database using SQL Server Management Studio.
1.	Open SQL Server Management Studio and connect to the target SQL Server instance.
2.	Right-click on the Databases node, and select Restore Database.
3.	Select Device and click the ellipses (...)
4.	In the dialog Select backup devices, click Add, navigate to the database backup in the filesystem of the server, and select the backup. Click OK.
5.	If needed, change the target location for the data and log files, in the Files pane. Note that it is best practice to place data and log files on different drives.
6.	Click OK. This will initiate the database restore. After it completes, you will have the AdventureWorks database installed on your SQL Server instance.

## Python
### Local installation (for Windows)
1.	Download and install **[Python](https://www.python.org/downloads/)** (any version of Python > 3.7).
    - We do not recommend using other python distributions (e.g. anaconda).
    - During installation, **add Python to your environmental variables**. That means that you have to check the box saying **ADD TO PATH** on the first screen during the installation
    - If prompted select to additionally install pip.
2.	Verify that Python is installed.
    - Open a command prompt and type the command for launching a python interpreter. Depending on the OS and python's version this can either be python, python3, py or py3.
    - If none work, you need to add python to your environmental variables manually. To do this, find the interpreter in the installation directory and **[add it as an environmental variable](https://www.computerhope.com/issues/ch000549.htm)**.
    - From now on we'll consider that python is installed and works with the command python. If this differs in your PC, use your own instead of python from now on.
3.	Verify that pip is installed.
    - Pip is a package manager for Python.
    - Open a command prompt and type the command pip.
    - If it doesn't exist type python -m pip. If this works, you can add pip to your environmental variables (look above on how to do this). `
    - If pip isn't installed, **[download the installer](https://bootstrap.pypa.io/get-pip.py)** and run it as a Python scripy: python get-pip.py.
4.	**[Download requirements.txt](https://github.com/codehub-learn/development-environment-setup/blob/main/requirements.txt)** and install them with pip: **pip install -r requirements.txt**.

### Local (Other OS)
Install python and pip through the OS's default package manager. Then run step 4 from before.  

*Note: Most linux and OSX distributions have some version of Python 2 preinstalled. Python version 2 and early versions of Python 3 are NOT compatible with what we will be seeing in this course. You must install Python version 3.7 or above locally.*

### Development Editor for Python
**[Download Visual Studio Code](https://code.visualstudio.com/)** and install.  
&nbsp;   
**Installation Instructions**
- **[Windows](https://code.visualstudio.com/docs/setup/windows)**
- **[MacOS](https://code.visualstudio.com/docs/setup/mac)**
- **[Linux](https://code.visualstudio.com/docs/setup/linux)**

## RabbitMQ
**[Download RabbitMQ](https://www.rabbitmq.com/download.html)** and install.  
For the installation you will be guided by the instructors of the academy. 



