# Hardware and software requirements for Jakarta EE + Angular framework development
&nbsp;
&nbsp;

## Workstation specifications, minimum requirements
- Windows 10 or later, Linux or MacOS, 64 bit
- RAM, 8GB required, 16GB preferable
- 128 GB Storage (SSD would be preferrable)
- 2 Core CPU

## Java Development Kit
1. Download and install the Java LTS version 21 from **[JDK 21 downloads](https://www.oracle.com/java/technologies/downloads/)** (free software).
2. In Windows, create an environment variable named **JAVA_HOME** pointing to JDK installation folder.

Earlier versions of Java are not compatible with the course content, you will need to have version 21. If you already have an earlier version of Java on you machine, you do not need to uninstall it. You can let it be used and install version 21 along with it.

## NetBeans IDE for Java Development
1. Download the latest version of **[Apache NetBeans](https://netbeans.apache.org/front/main/index.html)** for your operating system and install (free software). If, at any point of the installation, you are asked for the default version of Java to use, select the Java version 21 that you installed in the previous step.

If you prefer to use a different IDE, that is fine; support in the training, however, can only be provided for NetBeans. 

## Relational DBMS
1. Download and install the latest version of **[MySQL Community Server](https://dev.mysql.com/downloads/mysql/)** (free software).
2. Download and install the latest version of **[MySQL Workbench](https://dev.mysql.com/downloads/workbench/)** (free software).

## Jakarta Application Server
1. Download the zip file with the latest version of **[WildFly](https://www.wildfly.org/downloads/)**. Set a folder in your system where the zip file will be unzipped. WildFly does not require any installation, so you can unzip in any folder that you have write access.

## VSCode for Angular
1. Download and install the [VSCode](https://code.visualstudio.com/download) editor (free software).
2. Download and install an **LTS** version of [Node.js](https://nodejs.org/) (free software).

Angular applications require an LTS version of Node.js in order to work properly; non-LTS versions will not work as required. To verify that you have installed Node.js correctly, type the command `node -v` in a command line window and you should see the installed version of Node.js

For Windows users: if the previous command gives an error, verify that the path of the node executable has been added to your PATH environment variable.

## NPM

**Npm** is already included in Node.js. To verify that you have it, type the command `npm -v` in a command line window and you should see the installed npm version.

For Windows users: if the previous command gives an error, verify that the path of the npm executable has been added to your PATH environment variable.

## Other tools
1. Download and install **[Git Version Control](https://git-scm.com/downloads)** (free software). If you do not have the latest version of git, it is highly recommended that you update to the latest version.
2. Create a **[Github account](https://github.com/join)** if you don't already have one (free to create).

## Verification of Angular setup

To verify that you have setup your local Angular environment correctly, follow the steps below.

1. Clone this repository locally by running the command:

   ```sh
   git clone https://github.com/codehub-learn/angular-starter-kit.git
   ```

2. Navigate to the newly created `angular-starter-kit` folder and install the project dependencies:
   ```sh
   cd angular-starter-kit
   npm install
   ```

3. Run the **Angular Starter Kit** application using the command:
    ```sh
   ng serve -o
   ```
   You should see the following:

<p align="center">
  <img src="images/angular_app.png" alt="Angular Starter Kit is running" />
</p>

## Congratulations 👏

You are now ready to learn how to develop Jakarta + Angular applications with Code.Hub 🔥
