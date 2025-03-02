# **Aries**

Undergraduate Computer Science Thesis

# **Tools**

[CamQ](https://github.com/NebularEclipse/CamQ)


# **Guide**
# **Setting Up a Virtual Environment in Python**  
## **1. Create a Virtual Environment**  
To create a virtual environment, run the following command in your terminal:  

```sh
python -m venv venv
```

This will create a directory named `venv`, which contains the necessary files for an isolated Python environment.  

---

## **2. Activate the Virtual Environment**  
### **Windows**  
Run the following command:

```sh
venv\Scripts\activate
```

### **Linux/macOS**  
Use the following command:  

```sh
source venv/bin/activate
```

---

## **3. Verify the Virtual Environment Activation**  
Once activated, your terminal prompt should change to indicate that you are working inside the virtual environment.

You can confirm by checking the Python interpreter being used:  

```sh
python -c "import sys; print(sys.executable)"
```

The output should point to the `venv` directory rather than the system-wide Python installation.  

---

## **4. Deactivate the Virtual Environment**  
To exit the virtual environment, simply run:  

```sh
deactivate
```

---

# **Installing Dependencies in a Virtual Environment**  
## **1. Create a `requirements.txt` File**  
A `requirements.txt` file contains a list of dependencies that can be installed in a Python environment. To create one, run:  

```sh
pip freeze > requirements.txt
```

This will generate a file listing all installed packages in the current environment.  

Alternatively, you can manually create `requirements.txt` and add package names, one per line:  

```
flask
numpy
pandas
requests
```

---

## **2. Install Dependencies from `requirements.txt`**  
Once the virtual environment is activated, install all required packages using:  

```sh
pip install -r requirements.txt
```

This ensures that all dependencies are installed in the virtual environment.  

---

## **3. Verify Installed Packages**  
After installation, check if the required packages are installed correctly:  

```sh
pip list
```

---

## **4. Updating Dependencies**  
To update all dependencies to their latest versions, use:  

```sh
pip install --upgrade -r requirements.txt
```

If you need to update a **specific package**, run:  

```sh
pip install --upgrade package_name
```

---

## **5. Uninstall Dependencies**  
To remove all installed packages and reset the environment, run:  

```sh
pip uninstall -r requirements.txt -y
```

---