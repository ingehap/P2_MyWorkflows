# Infrastructure for Python and Julia on Windows 10

## 1. Python and Julia interpreters

Python and Julia interpreters are located here:
- C:\Program Files\Python310
- C:\Program Files\Python311
- C:\Program Files\Python312
- C:\Users\inp\AppData\Local\Programs\Julia-1.10.4\bin\julia.exe

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

## 5. Python Libraries Installed for Various Environments

### 5.1 Overview

For the moment, I have the following ten environments to ten subject-specific topics:

| Env Name     | Topic               | Size (GB)   |  Libraries                                                                                                         |
| ------------ | ------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------ |
| env312_CS_AI | AI                  | 4.4         | catboost keras openai pycaret pykan scikit-learn sketch tensorflow torch torchvision torchaudio xgboost jupyterlab |
| env312_CS_DA | Data Analysis       | 1.5         | dtale giddy missingno numpy pandas pingouin polars pykrige pylops scipy ydata-profiling jupyterlab                 |
| env312_CS_DB | Database            | 0.4         | beautifulsoup4 oracledb openserver pyodbc SQLAlchemy tagreader jupyterlab                                          |
| env312_CS_DV | Data Visualization  | 0.9         | dash folium ipywidgets matplotlib plotly seaborn streamlit sweetviz webviz jupyterlab                              |
| env312_CS_WR | Code Wrapper        | 0.2         | cython jupyterlab                                                                                                  |
| env312_ES_FP | Fluid Properties    | 0.8         | open_petro_elastic CoolProp neqsim[interactive] jupyterlab                                                         |
| env312_ES_GS | GeoScience          | 0.8         | burnman dlisio gempy geoapps georunes geostatspy lasio pysand rockphypy segyio striplog welly jupyterlab           |
| env312_ES_MS | Material Science    | 0.8         | pymatgen jupyterlab                                                                                                |
| env312_F     | Finance             | 0.9         | QuantLib QuantStats Riskfolio-Lib skfolio yfinance jupyterlab                                                      |
| env312_M     | Mathematics         | 0.9         | nimfa pmdarima prophet pytensor sktime smoothie sympy jupyterlab                                                   |

### 5.2 Links to documentation and GitHub

| Library            | Documentation                                        | GitHub                                                 |
| ------------------ | ---------------------------------------------------- | ------------------------------------------------------ |
| catboost           | [Link](https://catboost.ai)                          | [Link](https://github.com/catboost)                    |
| keras              | [Link](https://keras.io)                             | [Link](https://github.com/keras-team/keras)            |
| open_petro_elastic | [Link](https://equinor.github.io/open_petro_elastic) | [Link](https://github.com/equinor/open_petro_elastic)  |
| openai             | [Link](https://platform.openai.com/docs/overview)    | [Link](https://github.com/openai/openai-python)        |
| yfinance           | [Link](https://aroussi.com/tag/yfinance)             | [Link](https://github.com/ranaroussi/yfinance)         |

## 6. Jupyter Lab Launchers

Example with jupyteryxy_NAME.bat:
```python
call "C:\Appl\envxyz_NAME\Scripts\activate.bat"
cd "C:\Users\inp\OneDrive - Equinor\pythonxyz"
jupyter lab
```

## 7. Summary

The following infrastructure emerges based on the workflow above:

| *Item*                  | *Implementations*                             |
| ----------------------- | --------------------------------------------- |
| Environments for Python | C:\Appl\envxyz_NAME                           |
| Jupyter launchers       | C:\Appl\jupyterxyz_NAME.bat                   |
| OneDrive Work Areas     | C:\User\inp\OneDrive - Equinor\pythonxyz_NAME |
| Data Storage Area       | D:\Data\                                      |
| GitHub DeskTop          | D:\GitHub.lnk                                 |
| REPL for Julia          | D:\Julia 1.10.4.lnk                           |
| REPLs for Python        | D:\pythonxyz.lnk                              |

## 8. A Requirement File for Environment my_envxyz_NAME

The resulting file of running "pip freeze > requirementsxyz_NAME.txt".

## 9. Reference
- [10 minutes to pandas](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html)
- [CodeAcademy](https://www.codecademy.com/)
- [Equinor Wiki - OpenServer](https://wiki.equinor.com/wiki/OpenServer)
- [Equinor Wiki - ResScript](https://wiki.equinor.com/wiki/ResScript)
- [Equinor Wiki - Software:Python](https://wiki.equinor.com/wiki/Software:Python)
- [Equinor Wiki - Software:Python_coding_standard](https://wiki.equinor.com/wiki/Software:Python_coding_standard)
- [Equinor Wiki - Software:Python_Scientific](https://wiki.equinor.com/wiki/Software:Python_Scientific)
- [Python, Official Documentation](https://docs.python.org/)
- [Slack, Python channel](https://app.slack.com/client/T02JL00JU/C68CNC0M7)
- [Viva Engage - Python](https://engage.cloud.microsoft/main/groups/eyJfdHlwZSI6Ikdyb3VwIiwiaWQiOiIxMDE0NDE4MiJ9/all)
- [Viva Engage - Subscript](https://engage.cloud.microsoft/main/org/statoil.com/groups/eyJfdHlwZSI6Ikdyb3VwIiwiaWQiOiI3MjM0NTE3In0/all)

## Appendix A - Metadata about Python libraries

## Appendix B - Problems with installation

When installing the geoscience libraries pygcc and pygmi I get the following error message:
```cpp
Microsoft Visual C++ 14.0 or greater is required.
Get it with "Microsoft C++ Build Tools":
https://visualstudio.microsoft.com/visual-cpp-build-tools/
```

## Appendix C - Windows Environment Variables

Use Windows Search Toolbar to search for var/edit the system environment variables. The following variables have been set:

| *Variable*          | *Value*                                       |
| ------------------- | --------------------------------------------- |
| ORACLE_HOME         | C:\oracle12                                   |
| LD_LIBRARY_PATH     | C:\oracle12\ora19_64\lib:$LD_LIBRARY_PATH     |
| OneDrive            | C:\Users\inp\OneDrive - Equinor               |
| OneDrive Commercial | C:\Users\inp\OneDrive - Equinor               |
| TEMP                | C:\Users\inp\AppData\Local\Temp               |
| TMP                 | C:\Users\inp\AppData\Local\Temp               |

## Appendix D - Useful Windows commands related to Python

| *Command*               | *Meaning*                        |
| ----------------------- | -------------------------------- |
| pip --version           | Version of pip                   |
| python -m venv ENV_NAME | Make an environment              |
| where python            | Location of Python intepreter    |


