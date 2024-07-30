# Infrastructure Description

## Python intepreters:
They are on the form C:\Program Files\Pythonxyz, i.e, in our case
- C:\Program Files\Python310
- C:\Program Files\Python311
- C:\Program Files\Python312

## Workflow for making environments for Python intepreters, example Python310:
- F:\>C:
- C:\>cd "C:\Program Files\Python310"
- C:\Program Files\Python310>python -m venv C:\appl\my_env3.10.11
- C:\Program Files\Python310>cd C:\appl\my_env3.10.11\Scripts
- C:\Appl\my_env3.10.11\Scripts>activate
- (my_env3.10.11) C:\Appl\my_env3.10.11\Scripts>cd "C:\Program Files\Python310"
- (my_env3.10.11) C:\Program Files\Python310>python -m pip install --upgrade pip
- (my_env3.10.11) C:\Program Files\Python310>pip install ipython numpy pandas jupyter notebook segyio matplotlib

## Deactivate
- cd "C:\Appl\my_env3.10.11\Scripts"
- (my_env3.10.11) C:\Appl\my_env3.10.11\Scripts>deactivate

## Python libraries for Pythonxyz are stored here (hidden):
- c:\users\inp\appdata\roaming\python\pythonxyz\site-packages

## Summary
The following infrastructure emerges based on the workflow above:

| Python intepreter                     | Jupyter launcher           | OneDrive Work Area                           |
| ------------------------------------- | -------------------------- | -------------------------------------------- |
| C:\Program Files\Python310\python.exe | C:\Appl\jupyter3.10.11.bat | C:\user\inp\OneDrive - Equinor\python3.10.11 |
| C:\Program Files\Python311\python.exe | C:\Appl\jupyter3.11.9.bat  | C:\user\inp\OneDrive - Equinor\python3.11.9  |
| C:\Program Files\Python312\python.exe | C:\Appl\jupyter3.12.4.bat  | C:\user\inp\OneDrive - Equinor\python3.12.4  |

## Reference
- https://wiki.equinor.com/wiki/Software:Python
