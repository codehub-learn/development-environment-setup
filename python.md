# Starter Kit and Resources for Python

This course will be delivered using Jupyter Notebooks. There are two ways to use this tool: **locally** or **remotely**. 


## Local Setup

### Locally (for Windows)

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
5. Packages required during this course can be installed using the pip package manager. Either `pip install package-name` or `python -m pip install package-name`. Any package that is required will be pointed out in class.

### Locally (other OSs)

Install python and pip through the OS's default package manager. Then run step 4 from before.

*Note: Most linux and OSX distributions have Python 2 preinstalled. This is not compatible with what we will be seeing in this course. Either install Python 3 locally, or use the online tool described above!* 

You do not need to do anything else. You will install all the appropriate packages during the first session 

## Remote Setup (online) 

There are several online providers for hosting Jupyter notebooks. We recommend using **Google Colaboratory**.

Google Colaboratory is a cloud service that lets you create and edit python notebooks through the browser. You may write blocks of code (cells) and run them to get the output immediately, as well as cells of text (markdown) embedded with images, Latex etc. Also, you can install any python library you need, although most of them are already installed.

**Requirement**: google account (your gmail)

You can try it out [here](https://colab.research.google.com/notebooks/intro.ipynb)!




## Development IDE
**[Download PyCharm](https://www.jetbrains.com/pycharm/)** and install.

## Other tools
1. Git, download and install **[Git Version Control](https://git-scm.com/downloads)**
2. Create a **[Github account](https://github.com/join)**

