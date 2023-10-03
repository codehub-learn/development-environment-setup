# How to set up your PC for AZ-204 : Developing Solutions for Microsoft Azure
Here are the development tools **required** to enable you
to start.

## .NET Development Tools

1.  **[Visual Studio Community Edition](https://visualstudio.microsoft.com/vs/community/)**

During the installation select the workloads shown in red, below:

![workloads selection](images/vs-installation.png)

2.  [VS Code](https://code.visualstudio.com/)

## Database development

1.  You can download and install a SQL Server Local Installation OR you can use Docker ([SQL Server: Docker image](https://docs.microsoft.com/en-us/sql/linux/quickstart-install-connect-docker?view=sql-server-ver15&pivots=cs1-bash#pullandrun2019))
    - First [install Docker and cmder](#other-development-tools). Instructions on how to install Docker are below.
    - Open cmder and run the following command: 
    ```bash
    docker run -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=admin!@#123" -p 1433:1433 --name sql1 -d mcr.microsoft.com/mssql/server:2019-CU3-ubuntu-18.04
    ```
    - A new SQL Server instance will be created and you can access it using SQL Server Management Studio by using:

        Server name: `localhost`

        Authentication: `SQL Server authentication`

        Username: `sa`

        Password: `admin!@#123`

1.  You can use [SQL Server Management Studio](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15) 
    **or** [Azure Data Studio](https://docs.microsoft.com/en-us/sql/azure-data-studio/download-azure-data-studio?view=sql-server-ver15) for a UI.

### MS SQL Server Management Studio (SSMS)
If you choose to download SSMS, follow these steps:

1. Run the SSMS installer that you downloaded from above. You will need administrator access for this step.
2. It is possible that the installer will ask you to restart the machine. Let it do so. When the machine restarts, you will need to run the installer once again.
3. Once the installer completes, SSMS is ready to use. You can run SSMS from the start menu. The way to connect will be shown to you during the first training session.


## Docker

Docker installation instructions can be seen [in this link](https://docs.docker.com/desktop/install/windows-install/). If you do not want to study the instructions there, we have summarized the process that you need to follow in the next steps. The process will require administration access during many of the steps described here.

1. Download **Desktop Docker for Windows**

2. Run the Docker installer. **You will need administrator access for this step**.

3. The installer will give the option of “**Use WSL 2 instead of Hyper-V**” on a configuration page which it will show you. You **MUST** select the option of “Use WSL 2…”.  Because of this, the installer will install WSL 2, the Windows Subsystem for Linux. **You might need administrator access for this step**.

4. The installer will perform one or more restarts during installation. Once again, after your machine restarts **you might or might not be asked to need administrator access one more time for the installation to complete**.

5. When the installer is complete, you need to add your Windows name to a user group which can control Docker. To do so, start the **command prompt tool with administrator rights**. The folder/directory that you are in is not important. Simply type in the following command in it, **by replacing <user_name> with your Windows user name**
   ```
   net localgroup docker-users <user_name> /add
   ```                                                   
![image](https://user-images.githubusercontent.com/92853201/191688879-960e1b84-9bcd-41e7-aea1-514ecf81a5a6.png)

6.	When you run the above command, if you happen to get ‘System error 1378’ that ‘The specified account name is already a member of the group', **that is ok**, you do not need to worry.

7. You should now be able to start Docker Desktop from the start menu.





