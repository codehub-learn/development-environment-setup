# Generative and Agentic AI: Development Environment Setup Guide

## Python
**Download** and **install** the latest [Python](https://www.python.org/downloads/) vesrion.

> [!IMPORTANT]  
> During installation, **add python to your environmental variables**. That means that you have to check the box saying **ADD TO PATH** on the **first screen** during the installation

> [!NOTE]
> If prompted select to additionally install pip.

> [!CAUTION]
> We do **not** recommend using other python distributions (e.g. anaconda). 


1. Verify that python is installed.
    - Open a command prompt and type the command for launching a python interpreter. Depending on the OS and python's version this can either be `python`, `python3`, `py` or `py3`.
    - If none work, you need to add python to your environmental variables manually. To do this, find the interpreter in the installation directory and [add it as an environmental variable](https://www.computerhope.com/issues/ch000549.htm).
    - From now on we'll consider that python is installed and works with the command `python`. If this differs in your PC, use your own instead of `python` from now on.
1. Verify that pip is installed.
    - Open a command prompt and type the command `pip`.
    - If it doesn't exist type `python -m pip`. If this works, you can add pip to your environmental variables (look above on how to do this). `
    - If pip isn't installed, download the installer from [here](https://bootstrap.pypa.io/get-pip.py) and run it as a python script (on a terminal): `python get-pip.py`.

## pipx
Follow the instruction to install **[pipx](https://pipx.pypa.io/stable/installation/)** to your operating system
## Code editor
Feel free to use any IDE you like. **However, [VS Code](https://code.visualstudio.com/) is the recommended IDE** since it is light-weight, has a ton of extensions/plugins, and it is an industry standard. 


## Docker

1. Download **[Desktop Docker for Windows installer](https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe)**

1. Run the Docker installer. **You will need administrator access for this step**.

1. The installer will give the option of “**Use WSL 2 instead of Hyper-V**” on a configuration page which it will show you. You **BETTER** select the option of “Use WSL 2…”.  .

1. The installer will perform one or more restarts during installation. Once again, after your machine restarts.


### Node.js
Install the latest LTS version of **[Node.js](https://nodejs.org/en/)**
   - After installing node please verify that you have set up everything correctly by typing the below commands on your terminal:
        ```bash 
        node -v (any version above or equal 17 is fine)
        npm -v (any version or equal 7 is fine)
        ```
        
### Microsoft Authenticator
To access your azure account 2 Factor Authentication is required. Using your mobile device connect to your store and install **Microsoft Authenticator App**


### Git
1. Git, download and install **[Git Version Control](https://git-scm.com/downloads)**


## Accounts
1. There is no need to create an **MS Azure** account. One will be provided to you in class.
1. Create a **[Hugging Face account](https://huggingface.co/)**
1. Create a **[Postman account](https://www.postman.com/)**
1. Create a **[Github account](https://github.com/join)**


