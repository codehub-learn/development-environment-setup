# Starter Kit & Resources

---

## 1) Install Python

Download and install the latest stable **Python 3.14** from:  
https://www.python.org/downloads/

> [!IMPORTANT]  
> **Windows**: during installation, check **“Add Python to PATH”** on the first screen.

---

## Verify Python and pip

Open a terminal (Command Prompt / PowerShell / Terminal) and run:

```bash
python --version
# On macOS/Linux you may need: python3 --version
```

```bash
pip --version
# If this fails, try: python -m pip --version
```

## Common Issues

### “python is not recognized” (Windows)
Python was not added to PATH. Reinstall Python and check **Add to PATH**, or add it manually.

### “pip not found”
Use:

```bash
python -m pip --version
# Use pip via python -m
```


---

## 2) IDEs/Editor

You can any IDE/code editor. [VS Code](https://code.visualstudio.com/)  is preferred

### VS Code
- Lightweight and popular for Python development
- Works great with virtual environments

> [!IMPORTANT]
> Regardless of IDE, always make sure it uses the **Python interpreter
> from your `.venv`** (the respective virtual environment).

## Other tools
Git, download and install **[Git Version Control](https://git-scm.com/downloads)**


---

## 3) Databases (SQLite + PostgreSQL)

### SQLite (built-in)
SQLite requires **no server setup**. Python includes `sqlite3` by default.


### PostgreSQL (optional / when needed)
If you want PostgreSQL locally, install it from:  
https://www.postgresql.org/download/

Python driver for PostgreSQL:

```bash
python -m pip install psycopg2-binary
```
or

```bash
pip install psycopg2-binary
```

 

---

## 4) Accounts

### Create or use an Azure account 
An account at [azure](https://portal.azure.com) is needed

### Create or use a github account
Create a **[Github account](https://github.com/join)**

