# Starter Kit and Resources: Junior Software Commissioning Engineer

## Required Setup

- WSL2 (Windows only)
- Ubuntu 24.04 installed in WSL (Windows only)
- Windows Terminal (Windows only)
- VS Code 
- VS Code extensions
- Oracle account for FreeSQL access

## 1. Windows Subsystem for Linux (WSL2) + Ubuntu 24.04 (Windows only)

We will use **WSL2** as the Linux environment for the course, with **Ubuntu 24.04** as the standard Linux distribution. Please follow Microsoft's official WSL installation guide and install Ubuntu 24.04 when prompted, or use the distro-specific install command shown there.

- Official install guide: [Install WSL](https://learn.microsoft.com/en-us/windows/wsl/install)

Note: If you already have an older Ubuntu WSL installation, do not rely on it for the course unless instructed otherwise.

## 2. Windows Terminal

We recommend **Windows Terminal** as the main terminal application for the course. It provides a better command-line experience for working with PowerShell and WSL than the older Windows console.

- Official install page: [Install Windows Terminal](https://learn.microsoft.com/en-us/windows/terminal/install)

## 3. Visual Studio Code

We will use **Visual Studio Code (VS Code)** as the main editor for Linux scripts, SQL work, and C++ code. Please install the Windows version from the official download page.

- Official download page: [Download Visual Studio Code](https://code.visualstudio.com/download)

## 4. VS Code Extension: WSL

Please install the **WSL extension** for VS Code. This allows VS Code on Windows to open and edit files directly inside the Linux environment running under WSL.

- Extension page: [VS Code WSL Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl)
- Microsoft guide: [Use VS Code with WSL](https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode)

## 5. VS Code Extension: C/C++

Please install the **C/C++ extension** for VS Code. We will use it for the C++ part of the training.

- Extension page: [C/C++ for VS Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)
- Microsoft overview: [C/C++ in VS Code](https://code.visualstudio.com/docs/languages/cpp)

 For the cpp compiler, follow the steps
#### MSYS2  installation
- Download  msys2-x86_64-20260322.exe from: https://www.msys2.org
- Install it, use recommended configuration,  and open MSYS2 terminal
- Run: pacman -S mingw-w64-x86_64-gcc
- Add this folder to your PATH: C:\msys64\mingw64\bin
 

## 6. Oracle SQL Developer for VS Code

Please install **Oracle SQL Developer for VS Code**. We will use it for Oracle SQL and PL/SQL exercises.

- Official page: [Oracle SQL Developer for VS Code](https://www.oracle.com/database/sqldeveloper/vscode/)
- Download / marketplace page: [Install SQL Developer for VS Code](https://www.oracle.com/database/sqldeveloper/vscode/download/)

## 7. Oracle Account

Please create an **Oracle account** before the course. This will be needed to access Oracle's online SQL environment and related training tools.

- Create account: [Create an Oracle Account](https://profile.oracle.com/myprofile/account/create-account.jspx)

## 8. Oracle FreeSQL

For the Oracle labs, we will use **Oracle FreeSQL**, which runs in the browser and does **not** require a local Oracle Database installation on your laptop.

- Official page: [Oracle FreeSQL](https://www.oracle.com/database/technologies/oracle-free-sql/)
