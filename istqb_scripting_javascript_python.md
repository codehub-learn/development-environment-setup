# Hardware and software requirements for Scripting, JavaScript & Python
&nbsp;
&nbsp;

## Linux

For the Linux/Scripting session, two ways can be used. The first one is by using an online tool (requires no installation) or by using Docker (requires installation).

Docker will be used by the instructor within class.

### Docker

1. Download [Docker Desktop](https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe).
2. Follow the installation instructions to install Docker Desktop. For Windows, if you are running a supported system, Docker
   Desktop prompts you to enable WSL 2 during installation. Read the information displayed on the screen and enable WSL
   2 to continue.
3. Start Docker Desktop from the Windows Start menu.

## JavaScript

No installation required for the programming language.

### Code editor

Feel free to use any IDE you like. **However, [VS Code](https://code.visualstudio.com/) is the recommended IDE** since it is light-weight, has a tone of extensions/plugins, and it is an industry standard.

VS Code will be used within class.

## Python 

### Recommended Setup

- Python > 3.7
- Python packages:
    - jupyter
    - numpy

### How to set up your PC (locally)

#### Windows

1. Download and install [python](https://www.python.org/downloads/) (preferably python > 3.7).
    - We do **not** recommend using other python distributions (e.g. anaconda).
    - During installation, **add python to your environmental variables**. That means that you have to check the box saying **ADD TO PATH** on the first screen during the installation
    - If prompted select to additionally install pip.
2. Verify that python is installed.
    - Open a command prompt and type the command for launching a python interpreter. Depending on the OS and python's version this can either be `python`, `python3`, `py` or `py3`.
    - If none work, you need to add python to your environmental variables manually. To do this, find the interpreter in the installation directory and [add it as an environmental variable](https://www.computerhope.com/issues/ch000549.htm).
    - From now on we'll consider that python is installed and works with the command `python`. If this differs in your PC, use your own instead of `python` from now on.
3. Verify that pip is installed.
    - Pip is a package manager for Python.
    - Open a command prompt and type the command `pip`.
    - If it doesn't exist type `python -m pip`. If this works, you can add pip to your environmental variables (look above on how to do this). `
    - If pip isn't installed, download the installer from [here](https://bootstrap.pypa.io/get-pip.py) and run it as a python scripy: `python get-pip.py`.
4. Upgrade pip by running `pip install --upgarade pip` or `python -m pip install --upgrade pip`.
5. Packages that may be required during this course can be installed using the pip package manager. Either `pip install package-name` or `python -m pip install package-name`. Any package that may be required will be pointed out in class.

#### Other OS

Install python and pip through the OS's default package manager. Then run step 4 from before.

*Note: Most linux and OSX distributions have Python 2 preinstalled. This is not compatible with what we will be seeing in this course. Install Python 3 locally.*


#### Code Editor

See JavaScript section for code editor. The same will be used.

## Other tools
1. Git, download and install **[Git Version Control](https://git-scm.com/downloads)**
2. Create a **[Github account](https://github.com/join)**

