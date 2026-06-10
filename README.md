# **Best Practices for Virtual Environments**

## 1. Naming Conventions
- Use clear names like `venv`, `env`, or `project_env`.  
- Avoid generic names like `test` or `new`.

## 2. Keep requirements.txt Updated
~~~~~
pip freeze > requirements.txt
~~~~~
👉 Run this after adding/removing packages so teammates can install the same versions.

## 3. Use .gitignore
Add `myenv/` to `.gitignore` so the environment folder is not pushed to GitHub:
~~~~~
# Ignore virtual environment
myenv/
~~~~~

## 4. One Environment per Project
- Don’t reuse the same environment for multiple projects.  
- Each project should have its own isolated environment.

## 5. Use Specific Python Versions
- Create environments with the exact Python version your project requires:
~~~~~
python3.11 -m venv myenv
~~~~~

## 6. Deactivate When Done
- Always run `deactivate` before switching projects to avoid confusion.
