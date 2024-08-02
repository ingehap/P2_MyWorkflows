# Infrastructure for Python on Windows

If libraries have not been included yet, a comment saying so will be added.

## 1. Python intepreters

Python intepreters are located here:
- C:\Program Files\Python310
- C:\Program Files\Python311
- C:\Program Files\Python312

## 2. Storage of Libraries

Python libraries for the basic interpreters are stored here (hidden by company security policies):
- c:\users\inp\appdata\roaming\python\python310\site-packages
- c:\users\inp\appdata\roaming\python\python311\site-packages
- c:\users\inp\appdata\roaming\python\python312\site-packages

## 3. Workflow

Workflow for making environments envxyz_CS_AI for Python interpreter Pythonxyz (xyz = 310, 311, 312):
- "C:\Program Files\Pythonxyz\python" -m venv C:\Appl\envxyz_CS_AI
- C:\Appl\envxyz_CS_AI\Scripts\activate
- cd "C:\Program Files\Pythonxyz"
- python -m pip install --upgrade pip
- pip install list_of_libraries

## 4. Deactivate
- C:\Appl\env312_CA_AI\Scripts\deactivate

## 6. Libraries installed for various environments

### 6.1 envxyz_CS_AI (Artificial Intelligence)
- pip install catboost keras openai pycaret pykan sketch tensorflow torch torchvision torchaudio xgboost

### 6.2 envxyz_CS_DA (Data Analysis)
- pip install dtale giddy missingno numpy pandas pingouin polars pykrige ydata-profiling 

### 6.3 envxyz_CS_DV (Data Visualization)
- pip install folium ipython jupyter notebook jupyterlab ipywidgets matplotlib seaborn streamlit sweetviz 

### 6.4 envxyz_ES_FP (Fluid Properties)
- pip install open_petro_elastic CoolProp neqsim[interactive]

### 6.5 envxyz_ES_GM (Geo Modelling)
- pip install gempy

### 6.6 envxyz_ES_GP (Geophysics)
- pip install segyio

### 6.7 envxyz_ES_MS (Material Science)
- pip install pymatgen

### 6.8 envxyz_ES_PP (Petrophysics)
- pip install dlisio lasio striplog welly

### 6.9 envxyz_ES_RP (Rock Physics)
- pip install rockphypy 

### 6.10 envxyz_F (Finance)
- pip install QuantLib Riskfolio-Lib skfolio yfinance

### 6.11 envxyz_M_LA (Linear Algebra) 
- pip install nimfa pytensor

### 6.12 envxyz_M_TSA (Time Series Analysis)
- pip install pmdarima prophet sktime tsmoothie

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

- https://docs.python.org/
- https://engage.cloud.microsoft/main/groups/eyJfdHlwZSI6Ikdyb3VwIiwiaWQiOiIxMDE0NDE4MiJ9/all
- https://wiki.equinor.com/wiki/OpenServer
- https://wiki.equinor.com/wiki/Software:Python
- https://wiki.equinor.com/wiki/Software:Python_coding_standard
- https://wiki.equinor.com/wiki/Software:Python_Scientific


## Appendix A - Requirement file for environment my_env3.12.4

The resulting file of running "pip freeze > requirements3.12.4.txt" is attached.
