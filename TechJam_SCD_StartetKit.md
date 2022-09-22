# Starter Kit and Resources for Pfizer Tech Jam: Slowly Changing Dimensions

## Required Setup

- Docker
- Microsoft SQL Server
- Microsoft SQL Server Management Studio
- Tableau

## Install Docker

Docker installation instructions can be seen [in this link](https://docs.docker.com/desktop/install/windows-install/). If you do not want to study the instructions there, we have summarized the process that you need to follow in the next steps. The process will require administration access during many of the steps described here.

  1.	Download **Desktop Docker for Windows installer** (https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe, approximately 540 MB)

  2.	Run the Docker installer. **You will need administrator access for this step**.

  3.	The installer will give the option of “**Use WSL 2 instead of Hyper-V**” on a configuration page which it will show you. You **MUST** select the option of “Use WSL 2…”.  Because of this, the installer will install WSL 2, the Windows Subsystem for Linux. **You might need administrator access for this step**.

  4.	The installer will perform one or more restarts during installation. Once again, after your machine restarts **you might or might not be asked to need administrator access one more time for the installation to complete**.

  5.	When the installer is complete, you need to add your Windows name to a user group which can control Docker. To do so, start the **command prompt tool with administrator rights**. The folder/directory that you are in is not important. Simply type in the following command in it, **by replacing <user_name> with your Windows user name**
 
                                                        net localgroup docker-users <user_name> /add
                                                        
  ![image](https://user-images.githubusercontent.com/92853201/191688879-960e1b84-9bcd-41e7-aea1-514ecf81a5a6.png)

  6.	When you run the above command, if you happen to get ‘System error 1378’ that ‘The specified account name is already a member of the group', **that is ok**, you do not need to worry.

The installation is over and you should now be able to start Docker from the start menu; do so because it is needed for the **next installation**.

## Install MS SQL Server

To install the MS SQL Server inside Docker, you need to open a command prompt. **Administrator rights are NOT needed**. The folder/directory that you are in is not important. 
Type in the following command and wait for the installation to complete (approximately 700 MB).

                                               docker pull mcr.microsoft.com/mssql/server:2022-latest
                                               
  ![image](https://user-images.githubusercontent.com/92853201/191690060-ce86c1ca-591a-45a2-afd2-99026b0f51c8.png)

The MS SQL Server installation is complete inside Docker, but **you will not be able to connect to it yet** because you will need to create some user credentials for the server. **This connection process will be shown to you during the first training session.**

## Install MS SQL Server Management Studio (SSMS)

Download the installer for SSMS from [this link](https://aka.ms/ssmsfullsetup).

  1.	Run the SSMS installer. **You will need administrator access for this step**.
  2.	It is possible that the installer will ask you to restart the machine. Let it do so. When the machine restarts, you will need to **run the installer once again**.
  3.	Once the installer completes, SSMS is ready to use.
You can run SSMS from the start menu, but as explained earlier, it will not be possible to connect to the SQL Server yet. **This will be shown to you during the first training session**.

## Install Tableau

Download Tableau Desktop from Software on Demand. Further instructions regarding the academic license will follow.
