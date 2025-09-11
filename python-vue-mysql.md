# Starter Kit and Resources Python, Javascript, Vue and MySQL 



## Python

This training will be delivered using **Jupyter Notebooks**. There are two ways to use this tool: **locally** or **remotely**. 


### Local Setup

#### Locally for Windows

**Download** and **install** the latest [Python](https://www.python.org/downloads/) vesrion.

> [!IMPORTANT]  
> During installation, **add python to your environmental variables**. That means that you have to check the box saying **ADD TO PATH** on the **first screen** during the installation

> [!NOTE]
> If prompted select to additionally install pip.

> [!CAUTION]
> We do **not** recommend using other python distributions (e.g. anaconda). 

Next

1. Verify that python is installed.
    - Open a command prompt and type the command for launching a python interpreter. Depending on the OS and python's version this can either be `python`, `python3`, `py` or `py3`.
    - If none work, you need to add python to your environmental variables manually. To do this, find the interpreter in the installation directory and [add it as an environmental variable](https://www.computerhope.com/issues/ch000549.htm).
    - From now on we'll consider that python is installed and works with the command `python`. If this differs in your PC, use your own instead of `python` from now on.
2. Verify that pip is installed.
    - Pip is a package manager for Python.
    - Open a command prompt and type the command `pip`.
    - If it doesn't exist type `python -m pip`. If this works, you can add pip to your environmental variables (look above on how to do this). `
    - If pip isn't installed, download the installer from [here](https://bootstrap.pypa.io/get-pip.py) and run it as a python scripy: `python get-pip.py`.
3. Upgrade pip by running `pip install --upgarade pip` or `python -m pip install --upgrade pip`.
4. Packages required during this course can be installed using the pip package manager. Either `pip install package-name` or `python -m pip install package-name`. Any package that is required, like **jupyter** will be pointed out and installed in class.

#### Locally for other OSs

Install python and pip through the OS's default package manager. Then run step 4 from before.

*Note: Most linux and OSX distributions have Python 2 preinstalled. This is not compatible with what we will be seeing in this course. Either install Python 3 locally, or use the online tool described above!* 

You do not need to do anything else. You will install all the appropriate packages during the first session 


### Remote Setup (online) 

There are several online providers for hosting Jupyter notebooks. We recommend using **Google Colaboratory**.

Google Colaboratory is a cloud service that lets you create and edit python notebooks through the browser. You may write blocks of code (cells) and run them to get the output immediately, as well as cells of text (markdown) embedded with images, Latex etc. Also, you can install any python library you need, although most of them are already installed.

**Requirement**: google account (your gmail)

You can try it out [here](https://colab.research.google.com/notebooks/intro.ipynb)!


## Node.JS for Vue.js and Javascript

### Software Requirements

Before starting please make sure that you have successfully installed the below dependencies on your development environment.

- The latest **LTS** version of [Node.js](https://nodejs.org/en/) - Node.JS is a JavaScript runtime built on Chrome's V8 JavaScript engine.
- [npm](https://www.npmjs.com/) - is the official Nodejs Package Manager (npm) which allows the management of dependencies and packages. It is automatically installed with nodejs, so you don't have to install it separately.
- [Git](https://git-scm.com/) / [GitHub account](https://github.com/) - is a version control system for source code and GitHub is a community site that enables the easy creation and collaboration on Git projects.

### Verifying installation

After installing node please verify that you have set up everything correctly by typing the below commands on your terminal:

- `node -v` (any version above or equal 17 is fine)
- `npm -v` (any version or equal 7 is fine)

### Code editor 

Feel free to use any IDE you like. **However, [VS Code](https://code.visualstudio.com/) is the recommended IDE** since it is light-weight, has a tone of extensions/plugins, and it is an industry standard. 

VS Code will be used within class.


## MySQL RDBMS
1. Download and install the latest version of **[MySQL Community Server](https://dev.mysql.com/downloads/mysql/)** (free software).
2. Download and install the latest version of **[MySQL Workbench](https://dev.mysql.com/downloads/workbench/)** (free software).

## Other tools
1. Git, download and install **[Git Version Control](https://git-scm.com/downloads)**
2. Create a **[Github account](https://github.com/join)**

