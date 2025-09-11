# Starter Kit for ML production lab

## Recommended Setup

The main setup you'll need for this lab is:

- Python >= 3.10
- Python packages: 
  - FastAPI
  - uvicorn
  - Airflow

A detailed list of requirements can be found ...  
The lab was tested with Python 3.10.12, on the WSL environment of a Windows 11 PC.

## How to set up your PC

### Docker

1. Install docker engine in your computer.
    - For linux you can install this directly. Instructions can be found [here](https://docs.docker.com/engine/install/)
    - For Windows or MacOS install [docker desktop](https://docs.docker.com/desktop/) (this can also be installed in Linux, but I prefer just installing the engine).
2. If using docker desktop, start it once it's installed.
3. Run the airflow containers via docker compose.
    - The instructions for how docker can set up Airflow are all in a `docker-compose.yaml` yaml you can find [in the lab's repo](https://github.com/djib2011/teaching-material/tree/master/ml-production-lab).
    - Alternatively you can find the latest `docker-compose.yaml` for Airflow [here](https://airflow.apache.org/docs/apache-airflow/2.10.3/docker-compose.yaml); E.g. `curl -LfO 'https://airflow.apache.org/docs/apache-airflow/2.10.3/docker-compose.yaml'`
    - Open a terminal in the same location as `docker-compose.yaml` and run the command `docker compose up`

### Airflow standalone 

There have been a few bugs with this approach and therefore it is **not recommended** anymore!

#### Windows

The airflow standalone we will be using can be run only through WSL, so we'll need to perform all the installations in this WSL environment.

1. Install WSL.
   - In Windows 11 you can do so by opening powershell and typing `wsl --install`.
   - In older distributions the process might be slightly different.
   - More info can be found [here](https://learn.microsoft.com/en-us/windows/wsl/install).
2. Start a WSL terminal.  
   - By default, the previous step will install an ubuntu distribution.
   - Simply search the start menu for *ubuntu*. Click on the app to start up the WSL session.
![ubuntu-search.png](https://github.com/codehub-learn/development-environment-setup/blob/main/images/ml-production-lab/ml-production-lab/ubuntu-search.png?raw=true)
3. Inside the WSL terminal, follow the same installation instructions as the Linux section.
   - This will create a virtual environment and install the necessary libraries.

#### Linux / Mac

1. Make sure you have a working installation of python
   - I don't recommend using distributions like anaconda
   - The easiest way is to open a terminal and try to launch the interpreter (usually the command to do so is `python` or `python3`)
2. [Recommended] Create a virtual environment for our lab
   - This is cleaner than just installing packages to the system's default interpreter
   - You can do this by typing `python3 -m venv ml-env`. This will create a directory called `ml-env` which will host your virtual environment.
   - To activate the virtual environment type `source ml-env/bin/activate`.
   - Once activated, you will use and install packages to the virtual environment and not the system interpreter.
   - It's a good practice to upgrade the version of pip (so that it can find newer versions of libraries). Do this with `pip install --upgrade pip`
3. Install necessary packages.
   - You can find all the packages along with their versions [here]. Download this file (or clone the whole repo).
   - To install all packages you can run `pip install -r requirements.txt`

## Usage

### FastAPI

- You can find a dummy FastAPI script to test that everything is working ...
- Use the uvicorn command to launch the server. Syntax is `uvicorn script_name:app_name`. E.g. `uvicorn dummy_api:app`
- Open a browser and type `localhost:8000`. You should see the root page of your API
![fastapi.png](https://github.com/codehub-learn/development-environment-setup/blob/main/images/ml-production-lab/ml-production-lab/fastapi.png?raw=true)

### Airflow

#### Launching

- If you're using docker:
    - Open a terminal and go to the location of `docker-compose.yaml`
    - Run `docker compose up` and wait a bit until it says that the webserver is runnning
    - In this case login with the default credentials: username='airflow', password='airflow'.
- If using the standalone:
    - If properly installed, you should be able to run airflow by typing `airflow standalone`. This command
    - This will start up all airflow components (i.e. the scheduler, the webserver, etc.)
    - The username and password for airflow will be displayed in the terminal.
- Open a browser and type `localhost:8080`. You should see the Airflow UI
![airflow-ui.png](https://github.com/codehub-learn/development-environment-setup/blob/main/images/ml-production-lab/ml-production-lab/airflow-ui.png?raw=true)
- Do **not** close the terminal as long as you want to run airflow.
- To stop simply press CTRL+C in the terminal you launched the standalone.

#### Adding DAGs

- You can find a dummy dag to test your installation.
- There is a default location where you need to place DAG files in order to run them.
    - In the docker installation this should be inside the same directory as the `docker-compose.yaml`
    - In the standalone, this is controlled by the environment variable `AIRFLOW_HOME`. By default, it is in `~/airflow`.
- Inside this, you can create a directory called `dags`, under which you can place your DAGs.  
![dummy-dag-1.png](https://github.com/codehub-learn/development-environment-setup/blob/main/images/ml-production-lab/ml-production-lab/dummy-dag-1.png?raw=true)
- The DAG should appear in the UI shortly after.  
![dummy-dag-2.png](https://github.com/codehub-learn/development-environment-setup/blob/main/images/ml-production-lab/ml-production-lab/dummy-dag-2.png?raw=true)

## Other tools

### IDE

We will use the pycharm IDE for this lab, which can be found in the following link: **[Download PyCharm](https://www.jetbrains.com/pycharm/)** and install.

Feel free to use any other IDE that you are more comfortable with.

### Git

It will be helpful to set up git in your PC so that you can easily clone repos.

