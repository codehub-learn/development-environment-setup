# Hardware and software requirements for Java & Spring framework development, React and Oracle on Docker
&nbsp;
&nbsp;

## Java & Spring

### Workstation specifications
- Windows 10 or Linux or MacOS, 64 bit
- RAM, 8GB required, 16GB preferable
- 128 GB Storage (SSD would be preferrable)
- 4 Core CPU

### Development IDE
**[Download IntelliJ IDEA Ultimate](https://www.jetbrains.com/idea/download/#section=windows)** and install. In case you already have it installed and your license has expired, we will provide you a valid license for the duration of the course. In case you prefer using another IDE, that's also fine as the examples do not make use of any IDE specific functionality.

### Java Development Tools
1. Java Development Toolkit, download and install the latest LTS version **[JDK 17](https://bell-sw.com/)**. Create then an environmental variable named **JAVA_HOME** pointing to JDK installation folder.
2. Maven, download **[Maven](https://maven.apache.org/download.cgi)** and follow the **[instructions](https://maven.apache.org/install.html)**. Through Maven dependency management mechanism, we will download every library needed in our projects.  Create then an environmental variable named **MVN_HOME** pointing to Maven's installation folder.
3. Add **%JAVA_HOME%\bin** and **%MVN_HOME%\bin** to your **PATH** envrionmental variable.

### Other tools
1. Download and install **[Git Version Control](https://git-scm.com/downloads)**.
2. Create a **[Github account](https://github.com/join)**.

## React

### System Requirements

Before starting please make sure that you have successfully installed the below dependencies on your development environment.

- The latest **LTS** version of [Node.js](https://nodejs.org/en/) - Node.JS is a JavaScript runtime built on Chrome's V8 JavaScript engine.
- [npm](https://www.npmjs.com/) - is the official Nodejs Package Manager (npm) which allows the management of dependencies and packages. It is automatically installed with nodejs, so you don't have to install it separately.
- [git](https://git-scm.com/) / [GitHub account](https://github.com/) - is a version control system for source code and GitHub is a community site that enables the easy creation and collaboration on Git projects.

### Verifying installation

After installing node please verify that you have set up everything correctly by typing the below commands on your terminal:

- `node -v` ➡️ (any version above or equal 17 is fine),
- `npm -v` ➡️ (any version or equal 7 is fine).

### Code editor

Feel free to use any IDE you like. **However, [VS Code](https://code.visualstudio.com/) is the recommended IDE** since it is light-weight, has a tone of extensions/plugins, and it is an industry standard.

VS Code will be used within class with the following extensions:

- [Babel JavaScript](https://marketplace.visualstudio.com/items?itemName=mgmcdermott.vscode-language-babel)
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [npm Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.npm-intellisense)
- [Path Autocomplete](https://marketplace.visualstudio.com/items?itemName=ionutvmi.path-autocomplete)
- [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)
- [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

## Oracle (Standalone or Docker)

## 1) Oracle Standalone

Oracle Database Enterprise can be installed for free for non-commerical usage. Download and install Oracle Database 21c Enterprise Edition from the following link:
https://www.oracle.com/cis/database/technologies/oracle-database-software-downloads.html

**During installation do be careful to note the selected Pluggable Database (PDB) name and the password selected for the sys user, as they will be required in later steps.**

![db_install_snapshot](https://github.com/codehub-learn/development-environment-setup/blob/main/images/db_5a.png?raw=true)

*Note that a free Oracle account is required to proceed with the download*

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

See end for Oracle SQL Developer instructions.

## 2) Oracle with Docker

### Required Setup

- Docker
- Oracle Database Enterprise Edition
- Oracle SQL Developer

### Install Docker

Docker installation instructions can be seen [in this link](https://docs.docker.com/desktop/install/windows-install/). If you do not want to study the instructions there, we have summarized the process that you need to follow in the next steps. The process will require administration access during many of the steps described here.

1. Download **Desktop Docker for Windows installer** (https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe, approximately 540 MB)

2. Run the Docker installer. **You will need administrator access for this step**.

3. The installer will give the option of “**Use WSL 2 instead of Hyper-V**” on a configuration page which it will show you. You **MUST** select the option of “Use WSL 2…”.  Because of this, the installer will install WSL 2, the Windows Subsystem for Linux. **You might need administrator access for this step**.

4. The installer will perform one or more restarts during installation. Once again, after your machine restarts **you might or might not be asked to need administrator access one more time for the installation to complete**.

5. When the installer is complete, you need to add your Windows name to a user group which can control Docker. To do so, start the **command prompt tool with administrator rights**. The folder/directory that you are in is not important. Simply type in the following command in it, **by replacing <user_name> with your Windows user name**
   ```
   net localgroup docker-users <user_name> /add
   ```                                                   
![image](https://user-images.githubusercontent.com/92853201/191688879-960e1b84-9bcd-41e7-aea1-514ecf81a5a6.png)

6.	When you run the above command, if you happen to get ‘System error 1378’ that ‘The specified account name is already a member of the group', **that is ok**, you do not need to worry.

The installation is over and you should now be able to start Docker from the start menu; do so because it is needed for the **next installation**.

### Oracle Database Enterprise Edition on Docker Container

1. In order to download the oracle database through Docker, you need an Oracle account. Head to [this link](https://container-registry.oracle.com/ords/f?p=113:10).

2. While in the website, click on "Database -> enterprise" and you should be located in a page with the title "Oracle Database Enterprise Edition"

3. On the right side, there is a License Agreement you need to Accept. Before doing anything else, you are required to accept the license agreement. You can set English as the language.

4. Run docker, then open a terminal and write the following command to sign in with your Oracle account:
   ```docker
   docker login container-registry.oracle.com
   ```
5. Pull the Oracle EE image:
   ```docker
   docker pull container-registry.oracle.com/database/enterprise:21.3.0.0
   ```
6. Create a docker container from the image:
   ```docker
   docker run -d --name oracle-ee -p 1521:1521 container-registry.oracle.com/database/enterprise:21.3.0.0
   ```
7. The initialization phase of the image takes a long time (it might be 10 minutes or more), so in order to see the progress of the phase, write the following in the same terminal window you used to run the container:
   ```docker
   docker logs --follow oracle-ee
   ```
8. When the setup completes, open a new terminal window and run the following:
   ```docker
   docker exec oracle-ee ./setPassword.sh password1234
   ```
9. In the same terminal window, run the following command to connect directly to the container environment:
   ```docker
   docker exec -it oracle-ee sh
   ```
10. Then, start the database listener service using the following command:
    ```oraclesqlplus
    lsnrctl start
    ```
11. Next, you need to connect to the database. The command  is the following:
    ```oraclesqlplus
    sqlplus sys/password1234@ORCLCDB as sysdba
    ```

You connected to the Oracle Database Server and now you can use it.

### Oracle SQL Developer

Oracle SQL Developer is a free tool for interacting with the Oracle Database.

To be able to download it from the Oracle website, you will first need to have an account with Oracle or create a new account (it is free to do so).

Download Oracle SQL Developer (Windows 64-bit with JDK 11 included) from [this link](https://www.oracle.com/database/sqldeveloper/technologies/download/).

This is the portable format, so once the file has been downloaded, unzip it the location of your choice and the installation is complete. You can immediately run the executable. Make sure that the Docker container for Oracle is running, and you should be able to connect to it and send your SQL commands.

