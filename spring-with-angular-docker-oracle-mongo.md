# Hardware and software requirements for Spring framework development

&nbsp;
&nbsp;

## Workstation specifications

- Windows 10 or Linux or MacOS, 64 bit
- RAM, 16GB required, 32GB preferable
- 128 GB Storage (SSD would be preferrable)
- 4 Core CPU

## Development IDE

**[Download IntelliJ IDEA Ultimate](https://www.jetbrains.com/idea/download/#section=windows)** and install. In case you
already have it installed and your license has expired, we will provide you a valid license for the duration of the
course. In case you prefer using another IDE, that's also fine as the examples do not make use of any IDE specific
functionality.

## Java Development Tools

1. Java Development Toolkit, download and install the latest LTS version **[JDK 17](https://bell-sw.com/)**. Create then
   an environmental variable named **JAVA_HOME** pointing to JDK installation folder.
2. Maven, download **[Maven](https://maven.apache.org/download.cgi)** and follow
   the **[instructions](https://maven.apache.org/install.html)**. Through Maven dependency management mechanism, we will
   download every library needed in our projects. Create then an environmental variable named **MVN_HOME** pointing to
   Maven's installation folder.
3. Add **%JAVA_HOME%/bin** and **%MVN_HOME%/bin** to your **PATH** envrionmental variable.

## Angular

Starter kit for developing web apps with Code.Hub and Angular.
<p align="center">
  <img src="images/angular_logo.png" alt="Angular Starter Kit" />
</p>

The Recommended Setup includes the following software:

- Visual Studio Code (VSCode)
- Node.js
- npm

Find below the installation instructions:

1. Download and install [VSCode](https://code.visualstudio.com/download) editor.

2. Download and install an **LTS** version of [Node.js](https://nodejs.org/). To verify that you have installed it
   correctly type the command `node -v` in a command line window and it should display the installed version of Node.js
   > Angular applications require an LTS version of Node.js in order to work properly.
3. **Npm** is already included in Node.js. To verify that you have it, type the command `npm -v` in a command line
   window and it should display the installed npm version.
   > Windows users: if the previous command is not working, verify that the path of the npm executable has been added to
   your PATH environment variable.

To verify that you have set up your local environment correctly, follow the steps below.

1. Clone this repository locally by running the command:
   ```sh
   git clone https://github.com/codehub-learn/angular-starter-kit.git
   ```
2. Navigate to the newly created `angular-starter-kit` folder and install the project dependencies:
   ```sh
   cd angular-starter-kit
   npm install
   ```
3. Run the following command to install Angular CLI:
   ```sh
   npm install -g @angular/cli
   ```
   You should see the following:

4. Run the **Angular Starter Kit** application using the command:
    ```sh
   ng serve -o
   ```
   You should see the following:

<p align="center">
  <img src="images/angular_app.png" alt="Angular Starter Kit is running" />
</p>

## Other Tools

1. Download and install **[Git Version Control](https://git-scm.com/downloads)**.
2. Create a **[Github account](https://github.com/join)**.

## Software Servers

In order to complete the development environment landscape, we must install the **Oracle Database Express Edition**
and **MongoDB Community Server**. In order to both optimize the administration effort and align with development best
practices, we will use **Docker** to install them.

In the following section we will describe in details the process of setting up Docker on a Windows 10/11 machine, the
aforementioned servers and any accompanying software such as query editors.

### 1. Install Windows Subsystem for Linux 2 (WSL2)

1. Make sure your Windows installation has the latest updates installed.
   > **Settings > System > About > Windows Version = Windows 10 version 21H2**.
2. Open **Start**.
3. Search for  **Command Prompt**, right-click the top result, and select the  **Run as administrator**  option.
4. Type the following command to _install the WSL on Windows 10_ and press **Enter**:
   ```
   wsl --install
   ```
   ![Single command install WSL](https://i0.wp.com/pureinfotech.com/wp-content/uploads/2021/01/windows-10-wsl-install-single-command.jpg?resize=827%2C357&quality=78&strip=all&ssl=1)
5. Restart your computer to finish the WSL installation on Windows 10.
6. To set v2 as the default version for future installations, run:
   ```
   wsl.exe --set-default-version 2
   ```
7. Continue with the Linux distro setup as necessary.

Once you complete the steps, the required Linux components will automatically install the latest version of the Ubuntu
Linux distribution.

To update the WSL kernel to the latest version, use these steps:

1. Open  **Start**.
2. Search for  **Command Prompt**, right-click the top result, and select the  **Run as administrator**  option.
3. Type the following command to _update the WSL kernel_ and press **Enter**:
   ```
   wsl --update
   ```
   ![WSL update command](https://i0.wp.com/pureinfotech.com/wp-content/uploads/2021/01/wsl-update-command-windows-10.jpg?resize=827%2C202&quality=78&strip=all&ssl=1)

Once you complete the steps, if an update is available, then it will download and install on the device.

If the update command doesn’t work, open **Settings** > **Update & Security** > **Windows Update** > **Advanced
options**, and turn on the “**Receive updates for other Microsoft products when you update Windows”** toggle switch.

<u>**Note:**</u><br>
If you are receiving the error message "_Error: 0x80370102 The virtual machine could not be started because a required
feature is not installed._",
read [this article](https://www.thewindowsclub.com/error-0x80370102-the-virtual-machine-could-not-be-started).

Also, make sure **you haven't disabled virtualization in the BIOS**.

### 2. Install Docker for Windows 10

1. Go to [hub.docker.com](https://hub.docker.com/) and create your account, if you don't already have one.
2. Sign in and download [Docker Desktop](https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe).
3. Follow the usual installation instructions to install Docker Desktop. If you are running a supported system, Docker
   Desktop prompts you to enable WSL 2 during installation. Read the information displayed on the screen and enable WSL
   2 to continue.
4. Start Docker Desktop from the Windows Start menu.
5. From the Docker menu, select  **Settings**  >  **General**.
6. Select the  **Use WSL 2 based engine**  check box. If you have installed Docker Desktop on a system that supports WSL
   2, this option will be enabled by
   default.![Enable WSL 2](https://github.com/codehub-learn/development-environment-setup/blob/main/images/docker-settings-general.png?raw=true)
7. Click  **Apply & Restart**.
8. When Docker Desktop starts, go to  **Settings**  >  **Resources**  >  **WSL Integration**.
   The Docker-WSL integration will be enabled on your default WSL distribution. To change      
   your default WSL distro, run
   ```
   wsl --set-default <distro name>
   ```

   E.g., to set Ubuntu as your default WSL distro, run
   ```
   wsl --set-default ubuntu
   ```

   Optionally, select any additional distributions you would like to enable the Docker-WSL     
   integration on.

### 3. Install Windows Terminal (optional but really nice to have)

1. In Windows with WSL2, we strongly
   recommend [Windows Terminal](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701#activetab=pivot:overviewtab)
   from the Windows Store. It's a fantastic   
   Command Prompt replacement from Microsoft. Once you have it installed, also install   
   Ubuntu, or your favorite WSL2 Linux distribution from the Windows Store as well (or multiple
   distros), and you'll see a new Windows Terminal option to start a shell in that Linux distro. It's
   fast and feels Linux-native.
2. Additionally, we can
   install [Docker Completion for Powershell by Mat Gucci](https://github.com/matt9ucci/DockerCompletion) by issuing
   these commands:
   ```powershell
   Install-Module DockerCompletion -Scope CurrentUser
   Import-Module DockerCompletion
   ```
3. To make to Docker Completion start automatically every time we open a Powershell terminal,    
   we will make use
   of [PowerShell profile](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_profiles)
   by issuing these
   commands:
   ```powershell
   New-Item $PROFILE -ItemType File -Force
   Add-Content $PROFILE 'Import-Module DockerCompletion'
   ```

### 4. Install Oracle Software

1. Download [SQL Developer](https://download.oracle.com/otn/java/sqldeveloper/sqldeveloper-21.4.3.063.0100-no-jre.zip).
   Unzip the file and run the executable as it does not need installation.
2. Create a directory to host the database data files e.g. **$home/dbdata/oracle/oradata**.
3. Open a Powershell terminal and run the following command to download and run the latest **Oracle Database Express
   Edition** as a Docker image. Note that the **SYS_PASSWD** you are asked to provide is the password for the
   administration users **SYS** and **SYSTEM**.
   ```docker
   docker run -d --name xe -p 1521:1521 -e ORACLE_PASSWORD=<SYS_PASSWD> -v $home/dbdata/oracle/oradata:/opt/oracle/oradata gvenzl/oracle-xe:slim
   ```
4. Keep in mind that Oracle 21c XE has resource limitations: **2 CPU threads**. **2 GB of RAM**. **12GB of user data**.
5. We need to connect to the Oracle instance in order to create a user whom or application will use to connect to the
   database. To do this run
   ```docker
   docker exec -it xe bash -c "sqlplus /nolog"
   ```
6. Connect as DBA:
   ```oraclesqlplus
   connect sys as sysdba;
   ```
   and enter the password we passed as parameter in **step 2**.
7. Connect to Pluggable Database (PDB):
   ```oraclesqlplus
   alter session set container=xepdb1;
   ```
8. Create the user whose credentials will be assigned to the application we are going to develop, provide
   corresponding password and assign to him all privileges:
   ```oraclesqlplus
   alter session set "_ORACLE_SCRIPT"=true;
   create user <USERNAME> identified by <PASSWORD>;
   grant all privileges to <USERNAME>;
   ```
9. Connect using SQLDeveloper by defining as **Service** the value **XEPDB1**.
10. You are ready to interact with Oracle Database.

### 5. Install MongoDB Software

1. Create a directory to host the database data files e.g. **$home/dbdata/mongo**.
2. Open a Powershell terminal and run the following command to download and run the latest **MongoDB Community
   Server** as a Docker image. Note that the **MONGO_INITDB_ROOT_USERNAME** and **MONGO_INITDB_ROOT_PASSWORD** you are
   asked to provide are the administrator's credentials.
   ```docker
   docker run -d --name mongo -e MONGO_INITDB_ROOT_USERNAME=<USERNAME> -e MONGO_INITDB_ROOT_PASSWORD=<PASSWORD> -p 
   27017:27017 -v $home/dbdata/mongo:/data/db mongo --wiredTigerCacheSizeGB 0.5
   ```
3. Please note that by default, Mongo will set the **wiredTigerCacheSizeGB** to a value proportional to the host's total
   memory regardless of memory limits you may have imposed on the container. In such an instance you will want to set
   the cache size to something appropriate, taking into account any other processes you may be running in the container
   which would also utilize memory.
   See
   the [upstream "WiredTiger Options" documentation](https://docs.mongodb.com/manual/reference/program/mongod/#wiredtiger-options)
   for more details.
4. Download a client GUI to connect to MongoDB. You may choose [Mongo Compass](https://www.mongodb.com/products/compass)
   or [Studio3T](https://studio3t.com/). Connect using the credentials you provided above, connect, and you are
   ready to start using Mongo.
