# AI-Integrated Ambulance System

## 📌 Short Description
This project is an AI-integrated ambulance system developed using **Tkinter GUI** and **Machine Learning models** (Decision Tree, Random Forest, KNN).  
It includes a **Hospital Server GUI** and an **Ambulance Client GUI**, enabling real-time communication and patient condition classification.  
All implementation details, modules, and system requirements are described in the project documentation.

---

## 📑 Table of Contents
- [Prerequisites](#prerequisites-software--hardware)  
- [Download / Get the Package](#download--get-the-package)  
- [Local Setup](#local-setup)  
- [Installing Python & Dependencies](#installing-python--dependencies)  
- [Running the System](#running-the-system)  
- [Troubleshooting](#troubleshooting--common-notes)  
- [Project Notes](#project-notes-references--acknowledgements)

---

## 1) Prerequisites (Software & Hardware)

- **Python 3.7.x** (Recommended: 3.7.4; newer versions may work but this is the tested version)  
- IDE/Environment: **Python IDLE**, **Anaconda**, **Jupyter**, **VS Code**  
- Operating System: **Windows** or **Linux**  
- Minimum Hardware:  
  - Intel i3 (or equivalent)  
  - 4 GB RAM  
  - ~250 GB disk space  

---

## 2) Download / Get the Package

### Clone the Repository
```bash
git clone [https://your-repo-url.git](https://github.com/118bharath/AI-Integrated-Ambulance-System.git)
cd your-repo-name
OR Download ZIP
Download the ZIP file

Extract it

Navigate into the extracted project directory

Ensure datasets, scripts, and model files remain in the same project folder.

3) Local Setup
Create and activate a Python virtual environment:

Windows (PowerShell)
powershell

python -m venv venv
.\venv\Scripts\Activate.ps1
macOS / Linux (bash)
bash

python3 -m venv venv
source venv/bin/activate
4) Installing Python & Dependencies
4.1 Install Python
Download Python from:
https://python.org
(Ensure you check "Add Python to PATH" during installation.)

Verify installation:

bash

python -V
4.2 Install Dependencies
Create a requirements.txt file with:

nginx

numpy
pandas
matplotlib
seaborn
scikit-learn
tkinter is included with Python by default.
Linux users may need to install it manually:

bash

sudo apt install python3-tk
Install all dependencies:

bash

pip install -r requirements.txt
OR install individually:

bash

pip install numpy pandas matplotlib seaborn scikit-learn
5) Running the System
5.1 Locate Main Scripts
The project contains two main applications:

Hospital Server GUI
(File : hospital_server.py)

Ambulance Client GUI
(File : ambulance_client.py)

If filenames differ, search for:

main = tkinter.Tk() → GUI entry point

Socket server/client code → communication scripts

5.2 Start Hospital Server
bash

python hospital_server.py
This GUI allows you to:

Upload dataset (CSV)

Preprocess data

Train ML models (Decision Tree / Random Forest / KNN)

View confusion matrix & metrics

Start server-side communication

5.3 Start Ambulance Client
In a separate terminal (venv activated):

bash

python ambulance_client.py
The ambulance GUI allows:

Selecting test dataset

Predicting patient emergency category

Sending data to hospital server

Ensure:

The hospital server is running

IP address & port match between client and server

6) Troubleshooting & Common Notes
Tkinter error on Linux
Install:

bash

sudo apt install python3-tk
Client/server connection issues

Check firewall

Verify same HOST/PORT values in both scripts

CSV dataset issues

Expected format: features in columns + target as the last column

Rename your label column to target or update code accordingly

Python version mismatches

The system is tested on Python 3.7.4

Newer versions may require tweaking dependency versions

7) Project Notes, References & Acknowledgements
Refer to the project report for:

Software environment

System requirements

Detailed architecture

GUI screenshots

ML model implementation

Source code explanations
