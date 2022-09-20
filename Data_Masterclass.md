# Development Environment for Data Masterclass

## Development Editor
**[Download Visual Studio Code](https://code.visualstudio.com/)** and install.

### Installation Instructions
- **[Windows](https://code.visualstudio.com/docs/setup/windows)**
- **[MacOS](https://code.visualstudio.com/docs/setup/mac)**
- **[Linux](https://code.visualstudio.com/docs/setup/linux)**

Several plugins should be also installed during the course such as ESLint and Live Server.
Instructions on how to install and manage your plugins can be found here: **[Εxtension Marketplace](https://code.visualstudio.com/docs/editor/extension-gallery)**

## Data Visualization With Tableau
- Download and install the free trial of [Tableau Desktop](https://www.tableau.com/products/desktop/download).

## Software Stack for DevOps
1. Download and install **[Git Version Control](https://git-scm.com/downloads)**.
2. Download and install **[Java JDK 11](https://adoptopenjdk.net/)**.
3. Download and install **[VirtualBox](https://www.virtualbox.org/wiki/Downloads)**.
4. Download and install **[Visual Studio Code](https://code.visualstudio.com/)**.
5. Download and install **[PuTTY ssh client](https://www.putty.org/)**.
6. Download and install **[Docker](https://www.docker.com/products/docker-desktop)** **for project implementation**.
7. Download  **[Minikube](https://minikube.sigs.k8s.io/docs/start/)** **for project implementation**.
8. Download **[Jenkins LTS](https://www.jenkins.io/download/)**.
9. Download **[Prometheus](https://prometheus.io/download/)**.
10. Download **[Grafana](https://grafana.com/grafana/download)**.
11. Download **[Terraform](https://www.terraform.io/downloads.html)**.
12. Download **[CentOS 7.8.2003 - Graphical Desktop image](https://techloudgeek.com/download/image/?link=https://dl531.linuxvmimages.com/VirtualBox/C/7/CentOS_7.8.2003_VBG.zip)**
13. Download **[Ubuntu 20.04 LTS (Focal Fossa) image](https://techloudgeek.com/download/image/?link=https://dl531.linuxvmimages.com/VirtualBox/U/20.04/Ubuntu_20.04_VB.zip)**

### Additionally, create accounts in the following websites
1. Create a **[Github account](https://github.com/join)**.
2. Create an **[Azure Student account](https://azure.microsoft.com/en-us/free/students/)** with your Ath/Tech credentials.
3. Create a **[Docker Hub account](https://hub.docker.com/)**.
4. Create a **[Katacoda account](https://www.katacoda.com/)**.


## Data Iku Setup
- Install Data Iku using the ready-to-go Virtual Box appliance.
- Instructions are provided on [Data Iku's website](https://www.dataiku.com/product/get-started/virtualbox/).

## Recommended Setup for Python

- Python > 3.7
- Python packages: 
  - jupyter
  - numpy
  - pandas
  - matplotlib
  - seaborn
  - scikit-learn
  - imbalanced-learn
  - sktime

## How to set up your PC

The Python part of this academy will mostly be done on Jupyter Notebooks. There are two ways to use this tool: locally or online. 


### Online

There are several online providers for hosting Jupyter notebooks. We recommend using **Google Colaboratory**.

Google Colaboratory is a cloud service that lets you create and edit python notebooks through the browser. You may write blocks of code (cells) and run them to get the output immediately, as well as cells of text (markdown) embedded with images, Latex etc. Also, you can install any python library you need, although most of them are already installed.

**Requirement**: google account (your gmail)

You can try it out [here](https://colab.research.google.com/notebooks/intro.ipynb)!

We recommend using it through your google drive. You can set it up like this:

1. Sign in to your google account and visit your google drive.
2. Create a folder that will contain the notebooks that we will use in this course.
3. Connect colaboratory add-on to your google drive.

![](images/step1c.png)
![](images/step2c.png)
![](images/step3c.png)

4. Either upload an existing notebook and open it with colab or create a new one

![](images/step4c.png)

#### Pros:
- Environment is already setup, no need for installations/configurations.
- Pip and commonly used libraries are preinstalled.
- Processing is offloaded to a remote server, no need for computational power from your end.

#### Cons:
- Requires an internet connection.
- Slower than running it locally (in most cases).
- Data need to be uploaded to colab (or google drive).

#### Quickstart

![](images/step5c.png)

- Add a new code or text cell by clicking on the "+ Code" or "+ Text" button under the Menu bar
- Write a python command on a code cell (e.g. print ("hello world) )
- Run it by clicking the "play" button on the left of a code cell or by clicking Shift+Enter 
- To run an os command add "!" in the beggining (e.g. !pip3 list)
- Double-click on a text cell (markdown) in order to edit it
- You can use a GPU by selecting "Runtime -> Change runtime type" and setting the "Hardware accelerator"
- To upload a file to colab, click on the "Files" tab on the left, then click "Upload" and select a file
- You may also click on "Mount Drive" to get access to all your files on drive
- Install a python library using pip3 (e.g !pip3 install --upgrade scikit-learn)
- Import a library (e.g. import pandas)
- Download your code as a python file by selecting "File -> Dowload .py"
- Restart kernel (reset all variables) by selecting "Runtime -> Restart runtime..."

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
 4. Download **[requirements.txt](requirements.txt)** and install them with pip: `pip install -r requirements.txt`.

### Locally (other OS)

Install python and pip through the OS's default package manager. Then run step 4 from before.

*Note: Most linux and OSX distributions have Python 2 preinstalled. This is not compatible with what we will be seeing in this course. Either install Python 3 locally, or use the online tool described above!* 

## Other tools
1. Git, download and install **[Git Version Control](https://git-scm.com/downloads)**
2. Create a **[Github account](https://github.com/join)**
