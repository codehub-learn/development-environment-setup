# Starter Kit and Resources: Oracle Database Fundamentals Lab

## Required Setup

- Docker
- Oracle Database Enterprise Edition
- Oracle SQL Developer

## Install Docker

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

## Oracle Database Enterprise Edition on Docker Container

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

## Oracle SQL Developer

Oracle SQL Developer is a free tool for interacting with the Oracle Database. 

To be able to download it from the Oracle website, you will first need to have an account with Oracle or create a new account (it is free to do so). 

Download Oracle SQL Developer (Windows 64-bit with JDK 11 included) from [this link](https://www.oracle.com/database/sqldeveloper/technologies/download/). 

This is the portable format, so once the file has been downloaded, unzip it the location of your choice and the installation is complete. You can immediately run the executable. Make sure that the Docker container for Oracle is running, and you should be able to connect to it and send your SQL commands.
