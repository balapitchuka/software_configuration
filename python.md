# Python Configuration Management<a name="python-config-manage"></a>
Python environment setup and tools to manage multiple python software/versions

## References<a name="references"></a>
- [Python Implementations](https://wiki.python.org/moin/PythonImplementations)
- [Python Distributions Cpython](https://wiki.python.org/moin/PythonDistributions)
- [Python Implementations vs Distributions](https://stackoverflow.com/questions/27450172/python-implementation-vs-python-distribution-vs-python-itself)
- [Effective Python Environment](https://realpython.com/effective-python-environment/)


## Python Version Management(managing multiple versions of python on a machine)

### pyenv

pyenv is a mature tool for installing and managing multiple Python versions

**Important**  
Linux based OS comes with default python installed based on type/distribution of OS
+ If you want to install other versions use pyenv to manage them all


#### pyenv installation and setup
- [pyenv installtion](https://github.com/pyenv/pyenv-installer)


#### pyenv commands

##### List all the python versions and virtualenv present
  ```
  pyenv versions
  ```

##### Set global python version
  ```
  pyenv global 3.6.5
  ```

##### Set local python version
  ```
  pyenv local 3.7.8
  ```

##### Create virtual environement using specific python version
  ```
  pyenv virtualenv 3.6.7 env_name
  ```

##### Activate virtual environment
  ```
  pyenv activate env_name
  ```

##### Deactivate virtual environment
  ```
  pyenv deactivate
  ```

##### Run python scripts from pyenv virtualenvironment
  ```
  pyenv exec python3 -m pip freeze
  pyenv exec python3 hello.py
  ```



installing jupyter notebooks


### conda
open anaconda prompt after installation to type these commands

#### conda commands
##### Display Conda environment information
  ```
  conda info
  ```

##### Creating virtualenv using conda
  ```
  conda create -n my_virtualenv python=3.7

  conda create --name project-env python=3.7

  Note: The environments created by Conda is always located in /Users/.../anaconda3/envs/  (windows)
  ```

##### Activate virtual environment created using conda
  ```
  conda activate my_virtualenv
  ```

##### Deactivating virtual environment
  ```
  conda deactivate
  ```

##### Install dependencies from requirements.txt using conda
  ```
  conda install pip

  pip install -r requirements.txt
  ```

##### List all virtual environments managed by conda
  ```
  conda env list
  ```

##### Display all packages in the current virtual environment
  ```
  conda list
  ```

## Python Virtual Environment Management

### pipenv
Pipenv is a packaging tool for python that solves some common problems associated with typical workflow of pip, virtualenv, and requirements.txt file

virtualenv

venv


# Todo) How to resolve depedency version conflicts in pip and other package installers

