# Python Configuration Management<a name="python-config-manage"></a>
Python environment setup and tools to manage multiple python software/versions

## References<a name="references"></a>
- [Python Implementations](https://wiki.python.org/moin/PythonImplementations)
- [Python Distributions Cpython](https://wiki.python.org/moin/PythonDistributions)
- [Python Implementations vs Distributions](https://stackoverflow.com/questions/27450172/python-implementation-vs-python-distribution-vs-python-itself)
- [Effective Python Environment](https://realpython.com/effective-python-environment/)


## Python Version Management(managing multiple versions of python on a machine)

### pyenv<a name="pyenv"></a>

pyenv is a mature tool for installing and managing multiple Python versions

**Important**  
Linux based OS comes with default python installed based on type/distribution of OS
+ If you want to install other versions use pyenv to manage them all


#### pyenv installation and setup
- [pyenv installtion](https://github.com/pyenv/pyenv-installer)

Installation 
```bash

ubuntu

    sudo apt-get install -y make build-essential libssl-dev zlib1g-dev \
    libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
    libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl

    #Check out pyenv where you want it installed (PYENV_ROOT=$HOME/.pyenv)
    git clone https://github.com/pyenv/pyenv.git ~/.pyenv

    #Define environment variable PYENV_ROOT to point to the path where pyenv repo is cloned 
    #and add $PYENV_ROOT/bin to your $PATH for access to the pyenv command-line utility
    echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
    echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc

    # Add pyenv init to your shell to enable shims and autocompletion
    # Make sure eval "$(pyenv init -)" is placed toward the end of the shell configuration file
    # since it manipulates PATH during the initialization.
    # updated 2021/10/22
    # https://stackoverflow.com/questions/33321312/cannot-switch-python-with-pyenv
    echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init --path)"\nfi' >> ~/.bashrc

    #Restart your shell so the path changes take effect
    exec "$SHELL"

    #Install Python versions
    pyenv install --list       #list all available Python
    pyenv install 3.5.5        #install python3.5.5
    pyenv versions             #list all installed versions
    which python               #find the current location of the python interpreter
    pyenv which python         #show the actual location of the python interpreter it’s using
    #Uninstall
    pyenv uninstall 3.5.5

```


**pyenv commands**

List all the python versions and virtualenv present\.

  ```
  pyenv versions
  ```
1. List all the python versions and virtualenv present\.

  ```
  pyenv versions
  ```
1. Set global python version\.

  ```
  pyenv global 3.6.5
  ```
1. Set local python version\.
  ```
  pyenv local 3.7.8
  ```
1. Create virtual environement using specific python version\.
  ```
  pyenv virtualenv 3.6.7 env_name
  ```
1. Activate virtual environment
  ```
  pyenv activate env_name
  ```
1. Deactivate virtual environment
  ```
  pyenv deactivate
  ```
1. Run python scripts from pyenv virtualenvironment
  ```
  pyenv exec python3 -m pip freeze
  pyenv exec python3 hello.py
  ```

### pyenv refernces
- [Manage Multiple Python Versions with pyenv on Ubuntu and Mac](https://bizhishui.github.io/Manage-Pythons)

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
```
Install pipenv

pip install pipenv

Activate environment:
pipenv shell

Install dependencies:
pipenv install

```

pipenv references
[how pipenv works](https://realpython.com/pipenv-guide)

virtualenv

venv


# Todo) How to resolve depedency version conflicts in pip and other package installers



