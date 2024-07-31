# Infrastructure for Python on Windows

If libraries have not been included yet, a comment saying so will be added.

## 1. Storage of Libraries

Python libraries are stored here (hidden by companysecurity policies):
- c:\users\inp\appdata\roaming\python\python310\site-packages
- c:\users\inp\appdata\roaming\python\python311\site-packages
- c:\users\inp\appdata\roaming\python\python312\site-packages

## 2. Python intepreters

Python intepreters are located here:
- C:\Program Files\Python310
- C:\Program Files\Python311
- C:\Program Files\Python312

## 3. Workflow

Workflow for making environments for Python intepreters, example Python310:
- F:\>C:
- C:\>cd "C:\Program Files\Python310"
- C:\Program Files\Python310>python -m venv C:\appl\my_env3.10.11
- C:\Program Files\Python310>cd C:\appl\my_env3.10.11\Scripts
- C:\Appl\my_env3.10.11\Scripts>activate
- (my_env3.10.11) C:\Appl\my_env3.10.11\Scripts>cd "C:\Program Files\Python310"
- (my_env3.10.11) C:\Program Files\Python310>python -m pip install --upgrade pip
- (my_env3.10.11) C:\Program Files\Python310>pip install ipython numpy pandas jupyter notebook segyio matplotlib

## 4. Deactivate
- cd "C:\Appl\my_env3.10.11\Scripts"
- (my_env3.10.11) C:\Appl\my_env3.10.11\Scripts>deactivate

## 5. Additional ML packages to be installed (5)
- pip install jupyterlab catboost xgboost
- pip install tensorflow keras
- pip install torch torchvision torchaudio

## 6. Other packages (20)

### 6.0 AI (1)
- pip install sketch 

### 6.1 Data analysis (6)
- pip install dtale giddy missingno pingouin pykrige ydata-profiling 

### 6.2 Data visualization (5)
- pip install folium ipywidgets seaborn streamlit sweetviz 

### 6.3 Fluid properties (2)
- pip install open_petro_elastic 
- pip install neqsim[interactive]

### 6.4 Geomodelling (1)
- pip install gempy 

### 6.4 Petrophysics (4)
- pip install dlisio lasio striplog welly 

### 6.5 Rock physics (1)
- pip install rockphypy 

## 7. Jupyter Lab Launchers

Example with jupyter3.10.11.bat:
```python
call "my_env3.10.11\Scripts\activate.bat"
cd\ 
cd "Users\inp\OneDrive - Equinor\python3.10.11"
jupyter lab
```

## 8. Summary

The following infrastructure emerges based on the workflow above:

| Python intepreter                     | Jupyter launcher           | OneDrive Work Area                           |
| ------------------------------------- | -------------------------- | -------------------------------------------- |
| C:\Program Files\Python310\python.exe | C:\Appl\jupyter3.10.11.bat | C:\user\inp\OneDrive - Equinor\python3.10.11 |
| C:\Program Files\Python311\python.exe | C:\Appl\jupyter3.11.9.bat  | C:\user\inp\OneDrive - Equinor\python3.11.9  |
| C:\Program Files\Python312\python.exe | C:\Appl\jupyter3.12.4.bat  | C:\user\inp\OneDrive - Equinor\python3.12.4  |

## 9. Reference

- https://wiki.equinor.com/wiki/Software:Python
- https://docs.python.org/

## Appendix A - Requirement file for environment my_env3.12.4

The resulting file of running "pip freeze > requirements3.12.4.txt" is attached.
