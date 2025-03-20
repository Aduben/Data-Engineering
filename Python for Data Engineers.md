# Python Development Setup and Best Practices for Windows

This guide will help you set up Python development on your Windows machine and follow good practices while coding.

---

## 1. **How to Install Python on a Windows Machine and Prerequisites**

### Prerequisites:
Before installing Python, ensure you have these prerequisites:
- A Windows PC with a stable internet connection.
- Administrator privileges to install software on the system.

### Installation Steps:
1. **Download Python**: 
   Go to the official Python website [https://www.python.org/downloads/](https://www.python.org/downloads/) and download the latest stable version of Python for Windows.

2. **Run the Installer**:
   - Double-click the downloaded file to run the installer.
   - **Important**: Make sure you check the box that says **"Add Python to PATH"** before you click "Install Now". This ensures that Python is accessible from the command line.

3. **Verify the Installation**: 
   After installation, open the **Command Prompt** (Press `Win + R`, type `cmd`, and hit Enter). Type the following command:
   ```bash
   python --version
   This should display the installed Python version (e.g., Python 3.x.x).
4.	**Install pip (Package Installer for Python)**:
    Pip comes bundled with modern Python versions. To verify if pip is installed, run:
    pip --version
    If it's not installed, you can download it using the command:
    python -m ensurepip --upgrade
## 2. How to Install VSCode on a Windows Machine

1. **Download VSCode**: Visit [VSCode's download page](https://code.visualstudio.com/) and download the installer for Windows.

2. **Install VSCode**: Run the installer and follow the on-screen instructions. During installation, you may want to:
   - Check the option to **"Add to PATH"** so you can open VSCode from the command line.
   - Choose other options as per your needs (such as adding context menus).

3. **Launch VSCode**: After installation, you can launch VSCode from the Start Menu or by typing `code` in the command prompt if you added it to the PATH.

## 3. How to Run Python in VSCode and Important Extensions to Install

### Running Python in VSCode:

1. **Install Python Extension**:
   - Open VSCode, go to the Extensions view by clicking on the Extensions icon in the sidebar or pressing `Ctrl + Shift + X`.
   - In the search bar, type **"Python"** and install the official Python extension by Microsoft. This extension provides features like IntelliSense, linting, and debugging.

2. **Set Up a Python File**:
   - Create a new Python file by going to `File -> New File`, then save it with a `.py` extension (e.g., `hello.py`).
   - Type some Python code, for example:
     ```python
     print("Hello, World!")
     ```

3. **Run Python Code**:
   - You can run the Python file by pressing `Ctrl + Shift + P`, then typing **"Python: Run Python File in Terminal"**. Alternatively, you can click the green play button at the top right of the screen.

### Important Extensions:
- **Python** (official Microsoft extension): For coding assistance, IntelliSense, debugging, etc.
- **Pylint**: Linting extension that helps check for errors and enforces coding standards.
- **autopep8** or **black**: These extensions automatically format your Python code according to PEP 8 standards.
- **Jupyter**: If you want to work with Jupyter Notebooks inside VSCode.


## 4. The Use of Creating a Python Virtual Environment and How to Create It Using VSCode and CMD

### Why Use Virtual Environments:
- **Isolation**: A virtual environment helps isolate dependencies for different projects, preventing version conflicts between libraries.
- **Reproducibility**: Allows you to have an environment where you know exactly which packages and versions are installed.

### Creating Virtual Environment Using VSCode:

1. **Create a New Folder for Your Project**: Open VSCode and create a new folder or project directory.

2. **Open the Terminal in VSCode**:
   - Go to `Terminal -> New Terminal` (or use `Ctrl + ~`).
   - This will open a terminal window at the root of your project folder.

3. **Create the Virtual Environment**: In the terminal, run:
   ```bash
   python -m venv venv
   This will create a new virtual environment in a folder named venv.
4.	**Activate the Virtual Environment:**
-  For Windows: 
   -   .\venv\Scripts\activate
-  For macOS/Linux: 
   -    ource venv/bin/activate
After activation, you’ll see (venv) at the beginning of the command line, indicating the virtual environment is active.
### Creating Virtual Environment Using CMD:
1.	Open Command Prompt and navigate to your project directory.
2.	Run the following commands: 
3.	python -m venv venv
4.	.\venv\Scripts\activate
### Files Created in Virtual Environment:
-  venv/: The folder containing the isolated Python environment.
-  pyvenv.cfg: A configuration file within the venv/ folder.
-	Scripts/: Contains the Python executables and utilities like activate.
-	Lib/: Contains installed Python libraries and packages.
### Verifying the Virtual Environment:
-  To check that your virtual environment is active, run:
  -  which python  # On macOS/Linux
  -  where python  # On Windows
-  It should show the path pointing to your venv/ folder.
  
## The Use of Understanding the PATH  environment variable in Running Python

### The PATH Environment Variable
The **PATH** is an environment variable that tells the operating system where to look for executable files. When you install Python, adding Python to the PATH ensures that you can run `python` or `python3` from the command line.

---

### Why PATH Matters:
- **Running Python from Command Line**: Without Python in PATH, you would need to specify the full path to Python each time.
- **Installing and Running Packages**: Tools like `pip` depend on PATH to find Python executables and manage packages correctly.

---

### Checking Python’s PATH:
1. Open Command Prompt and type:
   ```bash
   echo %PATH%
This will display the directories listed in your PATH.
If Python is added correctly, you should see the path to the Python installation (e.g., C:\Python39).
### Fixing PATH Issues:
-	If Python is not in PATH, you can add it manually by modifying your system environment variables: 
-	Open the Start menu, search for “Environment Variables”.
-	Under System Properties, click Environment Variables.
-	In the System variables section, find Path, and click Edit.
-	Add the path to your Python installation (e.g., C:\Python39\ and C:\Python39\Scripts\).
Once done, close and reopen your terminal and type python --version to verify.

### Final Thoughts
-  Following these steps will help you get a proper Python environment set up on your Windows machine, making it easier to develop Python applications. 
-  Understanding the importance of virtual environments, the role of PATH, and using VSCode effectively will greatly enhance your productivity and help you follow best practices.
-  Keep experimenting with these tools and keep improving your coding skills!

