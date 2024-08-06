# Infrastructure for Python on Windows

If libraries have not been included yet, a comment saying so will be added.

## 1. Python interpreters

Python interpreters are located here:
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

| *Env Name*   | *Topic*             | *Size (GB)* | *Libraries*                                                                                           |
| ------------ | ------------------- | ----------- | ----------------------------------------------------------------------------------------------------- |
| env312_CS_AI | AI                  | 4.4         | catboost keras openai pycaret pykan sketch tensorflow torch torchvision torchaudio xgboost jupyterlab |
| env312_CS_DA | Data Analysis       | 1.5         | dtale giddy missingno numpy pandas pingouin polars pykrige ydata-profiling jupyterlab                 |
| env312_CS_DV | Data Visualization  | 0.8         | folium ipywidgets matplotlib seaborn streamlit sweetviz jupyterlab                                    |
| env312_ES_FP | Fluid Properties    | 0.8         | open_petro_elastic CoolProp neqsim[interactive] jupyterlab                                            |
| env312_ES_GM | GeoModelling        | 0.3         | gempy jupyterlab                                                                                      |
| env312_ES_GP | GeoPhysics          | 0.3         | segyio jupyterlab                                                                                     |
| env312_ES_MS | Material Science    | 0.8         | pymatgen jupyterlab                                                                                   |
| env312_ES_PP | PetroPhysics        | 0.6         | dlisio lasio striplog welly jupyterlab                                                                |
| env312_ES_RP | Rock Physics        | 0.6         | rockphypy jupyterlab                                                                                  |
| env312_F     | Finance             | 0.9         | QuantLib Riskfolio-Lib skfolio yfinance jupyterlab                                                    |
| env312_M_LA  | Linear Algebra      | 0.5         | nimfa pytensor jupyterlab                                                                             |
| env312_M_TSA |Time Series Analysis | 0.8         | pmdarima prophet sktime tsmoothie jupyterlab                                                          |

## 6. Jupyter Lab Launchers

Example with jupyteryxy_NAME.bat:
```python
call "C:\Appl\envxyz_NAME\Scripts\activate.bat"
cd "C:\Users\inp\OneDrive - Equinor\pythonxyz"
jupyter lab
```

## 7. Summary

The following infrastructure emerges based on the workflow above:

| *Item*              | *Implementations*                             |
| ------------------- | --------------------------------------------- |
| Data Storage Area   | D:\Data\                                      |
| GitHub DeskTop      | D:\GitHub.lnk                                 |
| Jupyter launchers   | C:\Appl\jupyterxyz_NAME.bat                   |
| OneDrive Work Areas | C:\User\inp\OneDrive - Equinor\pythonxyz_NAME |
| REPLs               | D:\pythonxyz.lnk                              |

## 8. A Requirement File for Environment my_envxyz_NAME

The resulting file of running "pip freeze > requirementsxyz_NAME.txt".

## 9. Reference
- [Equinor Wiki - OpenServer](https://wiki.equinor.com/wiki/OpenServer)
- [Equinor Wiki - ResScript](https://wiki.equinor.com/wiki/ResScript)
- [Equinor Wiki - Software:Python](https://wiki.equinor.com/wiki/Software:Python)
- [Equinor Wiki - Software:Python_coding_standard](https://wiki.equinor.com/wiki/Software:Python_coding_standard)
- [Equinor Wiki - Software:Python_Scientific](https://wiki.equinor.com/wiki/Software:Python_Scientific)
- [Python, Official Documentation](https://docs.python.org/)
- [Slack, Python channel](https://app.slack.com/client/T02JL00JU/C68CNC0M7)
- [Viva Engage - Python](https://engage.cloud.microsoft/main/groups/eyJfdHlwZSI6Ikdyb3VwIiwiaWQiOiIxMDE0NDE4MiJ9/all)
- [Viva Engage - Subscript](https://engage.cloud.microsoft/main/org/statoil.com/groups/eyJfdHlwZSI6Ikdyb3VwIiwiaWQiOiI3MjM0NTE3In0/all)
