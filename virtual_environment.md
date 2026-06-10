# **How to Create a Virtual Environment**

## 1. Create Environment
~~~~~
python -m venv myenv
~~~~~

## 2. Activate Environment
### Windows (CMD)
~~~~~
myenv\Scripts\activate
~~~~~

### Windows (PowerShell)
~~~~~
.\myenv\Scripts\Activate.ps1
~~~~~

### Linux / macOS
~~~~~
source myenv/bin/activate
~~~~~

## 3. Deactivate Environment
~~~~~
deactivate
~~~~~

## 4. Install Packages
~~~~~
pip install package_name
~~~~~

## 5. Save Dependencies
~~~~~
pip freeze > requirements.txt
~~~~~

## 6. Install from requirements.txt
~~~~~
pip install -r requirements.txt
~~~~~

## 7. Delete / Recreate Environment
### Linux / macOS
~~~~~
rm -rf myenv
~~~~~

### Windows CMD
~~~~~
rmdir /s myenv
~~~~~

---

# **Troubleshooting Virtual Environments**

## 1. PowerShell Activation Error
Error: *“Activate.ps1 is disabled on this system”*  
Fix: Run this command in PowerShell (Admin):
~~~~~
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
~~~~~

## 2. venv Module Not Found
Error: *“No module named venv”*  
Fix: Install Python’s venv package:
~~~~~
pip install virtualenv
~~~~~

## 3. Wrong Python Version
Error: *Environment uses old Python*  
Fix: Specify version explicitly:
~~~~~
python3.11 -m venv myenv
~~~~~

## 4. Package Not Found
Error: *“ModuleNotFoundError” after install*  
Fix: Ensure environment is active before installing:
~~~~~
myenv\Scripts\activate   # Windows
source myenv/bin/activate # Linux/macOS
pip install package_name
~~~~~
