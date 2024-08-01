# Installation of Python in home directory without sudo right

## Install Python

Get Python: wget http://www.python.org/ftp/python/2.7.7/Python-2.7.7.tgz

Uncompress the folder: tar -zxvf Python-2.7.7.tar.gz

Move inside the directory: cd Python-2.7.7

Create the destination folder: mkdir ~/.localpython

Prepare the environment for building: ./configure --prefix=/home/<username>/.localpython

Building the system: make

Implement the installation: make install

## Install the Virtual Environment

Get the virtual env.: wget http://pypi.python.org/packages/source/v/virtualenv/virtualenv-1.9

Uncompress the folder: tar -zxvf virtualenv-1.9.tar.gz

Move inside the directory: cd virtualenv-1.9/

Install the virtual environment for the local python: ~/.localpython/bin/virtualenv setup.py install

Create the Virtual Environment
Create a virtual environement using the local installation: virtualenv virtalenv_name -p /home/<username>/.localpython/bin/python2.7

Use the virutal env.: source ~/virtualenv-1.9/virtalenv_name/bin/activate

disconnect from the virtual env.: deactivate

## References

http://stackoverflow.com/questions/1534210/use-different-python-version-with-virtualenv

http://isezen.com/2011/09/02/how-to-install-locally-python-on-linux-home-directory/

http://opensourcehacker.com/2012/09/16/recommended-way-for-sudo-free-installation-of-python-software-with-virtualenv/

