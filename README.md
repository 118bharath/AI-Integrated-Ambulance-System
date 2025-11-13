# AI-Integrated-Ambulance-System

Short description
This project is an AI-integrated ambulance system (Tkinter GUI + ML models) that trains/classifies sensor/patient data (Decision Tree / Random Forest / KNN), hosts a hospital (server) GUI and communicates with ambulance client(s). The implementation, modules and system requirements are described in the project report. 

Table of contents

Prerequisites

Download / get the package

Local setup 

Installing Python & dependencies

Running the system (server & ambulance client)

Troubleshooting & tips

Project notes & references

1) Prerequisites (software & hardware)

Python 3.7.x (the report uses Python 3.7.4). If you use a later 3.x version it will most likely work but 3.7 is the tested version in the report. 


A typical environment / IDE: Python IDLE / Anaconda / Jupyter / VS Code. 


OS: Windows or Linux.

Minimum hardware: Intel i3 (or comparable), 4 GB RAM, ~250 GB disk (project doesn’t require huge storage). 


2) Download the package

If you have a compressed package (zip / tar) or a Git repo:

From Git:

# example
git clone https://your-repo-url.git
cd your-repo-name


If you received a zip file: extract and cd into the extracted folder.

(Place all code, datasets and any provided model files inside the same project folder.)

3) Local setup 

Create and activate a virtual environment to avoid dependency conflicts.

Windows (PowerShell)
# create venv
python -m venv venv

# activate
.\venv\Scripts\Activate.ps1

macOS / Linux (bash)
python3 -m venv venv
source venv/bin/activate

4) Install Python & project dependencies
4.1 Install Python

If Python is not installed, download from https://python.org
 and install (tick Add Python to PATH). The project report describes installing Python 3.7.4 and verifying with python -V. 


4.2 Create requirements.txt (suggested)

Based on the report and the source, the project uses these Python packages:

numpy
pandas
matplotlib
seaborn
scikit-learn
tk (tkinter comes with CPython; usually no pip install required)


Note: tkinter is typically bundled with standard CPython installations; on some Linux distributions you may need to install OS package python3-tk. The project also uses built-in modules like socket, pickle, and threading (no pip install).

You can create requirements.txt with the lines above, then run:

pip install -r requirements.txt


Or install individually:

pip install numpy pandas matplotlib seaborn scikit-learn


(If you use Anaconda, you may prefer conda install for some packages.)

Sources describing the modules used and Python environment are in the report.

5) Running the system locally
5.1 Locate main scripts

The report contains hospital (server) GUI source in Chapter 9 and describes an ambulance side GUI as well (figures and implementation). The server script uses Tkinter and scikit-learn to train models and open a GUI. Look for files such as:

hospital_server.py (or similarly named script containing main = tkinter.Tk() and the hospital/server logic)

ambulance_client.py (or similarly named script for the ambulance side)

The hospital/server code and ML GUI flow are shown in the report (Chapter 9).

If filenames differ in the package, open the .py files and look for main = tkinter.Tk() (server GUI) or socket client/server code to identify which file to run.

5.2 Example: run hospital (server)

With your virtual environment active and dependencies installed:

# from project root
python hospital_server.py


This should launch the Tkinter GUI where you can:

Upload dataset (CSV)

Preprocess, train Decision Tree / Random Forest / KNN

View metrics / confusion matrix and run the cloud/server socket listener (as implemented). 


5.3 Example: run ambulance client

Open a separate terminal (still with the venv activated) and run the ambulance script:

python ambulance_client.py


The ambulance client GUI will allow selecting test dataset and reporting to the hospital server (per the report’s figures). Ensure the server is running and that the client uses the correct server IP and port (check client source if you need to change addresses). 


6) Troubleshooting & common notes

tkinter errors on Linux: install OS package python3-tk (Debian/Ubuntu: sudo apt install python3-tk).

Port/address: If client‐server communication fails check firewall and that both processes use the same IP/port. The server code uses socket and Thread—verify the HOST/PORT values in the scripts. 


Dataset format: The GUI expects a CSV with features in columns and target as the last column (report examples show target column used for labels). If your CSV headers differ, either rename or update the target column reference in code. 

Python version issues: The report’s tested version is Python 3.7.4. Newer 3.x versions usually work but you may need to adjust minor package versions. 


7) Project notes, references & acknowledgements

The project report documents software environment, modules used, system requirements and shows the hospital server source and GUI screenshots. Please consult Chapter 6 (Software Environment), Chapter 7 (System Requirements) and Chapter 9 (Source Code) for in-depth details.

If you want, I can:
