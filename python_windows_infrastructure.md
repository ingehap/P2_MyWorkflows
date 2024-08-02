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

Workflow for making environments envxyz_NAME for Python interpreter Pythonxyz (xyz = 310, 311, 312 and NAME = CS_AI etc.):
- "C:\Program Files\Pythonxyz\python" -m venv C:\Appl\envxyz_NAME
- C:\Appl\envxyz_NAME\Scripts\activate
- cd "C:\Program Files\Pythonxyz"
- python -m pip install --upgrade pip
- pip install list_of_libraries

## 4. Deactivate
- C:\Appl\envxyz_NAME\Scripts\deactivate

## 5. Libraries Installed for Various Environments

### 5.1 envxyz_CS_AI (Artificial Intelligence)
- pip install catboost keras openai pycaret pykan sketch tensorflow torch torchvision torchaudio xgboost

### 5.2 envxyz_CS_DA (Data Analysis)
- pip install dtale giddy missingno numpy pandas pingouin polars pykrige ydata-profiling 

### 5.3 envxyz_CS_DV (Data Visualization)
- pip install folium ipython jupyter notebook jupyterlab ipywidgets matplotlib seaborn streamlit sweetviz 

### 5.4 envxyz_ES_FP (Fluid Properties)
- pip install open_petro_elastic CoolProp neqsim[interactive]

### 5.5 envxyz_ES_GM (GeoModelling)
- pip install gempy

### 5.6 envxyz_ES_GP (GeoPhysics)
- pip install segyio

### 5.7 envxyz_ES_MS (Material Science)
- pip install pymatgen

### 5.8 envxyz_ES_PP (PetroPhysics)
- pip install dlisio lasio striplog welly

### 5.9 envxyz_ES_RP (Rock Physics)
- pip install rockphypy 

### 5.10 envxyz_F (Finance)
- pip install QuantLib Riskfolio-Lib skfolio yfinance

### 5.11 envxyz_M_LA (Linear Algebra) 
- pip install nimfa pytensor

### 5.12 envxyz_M_TSA (Time Series Analysis)
- pip install pmdarima prophet sktime tsmoothie

## 6. Jupyter Lab Launchers

Example with jupyteryxy_NAME.bat:
```python
call "my_envxyz_NAME\Scripts\activate.bat"
cd\ 
cd "Users\inp\OneDrive - Equinor\pythonxyz_NAME"
jupyter lab
```

## 7. Summary

The following infrastructure emerges based on the workflow above:

| Python intepreter                     | 
| ------------------------------------- | 
| C:\Program Files\Python310\python.exe | 
| C:\Program Files\Python311\python.exe |
| C:\Program Files\Python312\python.exe | 

Jupyter launcher: C:\Appl\jupyterxyz_NAME.bat

OneDrive Work Area: C:\User\inp\OneDrive - Equinor\pythonxyz_NAME

## 8. Reference

- https://docs.python.org/
- https://engage.cloud.microsoft/main/groups/eyJfdHlwZSI6Ikdyb3VwIiwiaWQiOiIxMDE0NDE4MiJ9/all
- https://wiki.equinor.com/wiki/OpenServer
- https://wiki.equinor.com/wiki/Software:Python
- https://wiki.equinor.com/wiki/Software:Python_coding_standard
- https://wiki.equinor.com/wiki/Software:Python_Scientific


## Appendix A - Requirement file for environment my_envxyz_NAME

The resulting file of running "pip freeze > requirementsxyz_NAME.txt" is attached.
