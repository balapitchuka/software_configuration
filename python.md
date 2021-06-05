# Python Software Setup and Configuration 


## Python Version Management(managing multiple versions of python on a machine)

### pyenv

pyenv is a mature tool for installing and managing multiple Python versions

**Note**
Linux based OS comes with default python installed based on type/distribution of OS
- If you want to install other versions use pyenv to manage them all

Install and configure pyenv

List all the python versions and virtualenv present
```
pyenv versions
```

Set global python version
> pyenv global 3.6.5

Set local python version
>pyenv local 3.7.8

Create virtual environement using specific python version
> pyenv virtualenv 3.6.7 env_name

Activate virtual environment
> pyenv activate env_name

Deactivate virtual environment
> pyenv deactivate




installing jupyter notebooks


### conda
open anaconda prompt after installation to type these commands

 Display Conda environment information
 > conda info

Creating virtualenv using conda
> conda create -n my_virtualenv python=3.7

>  conda create --name project-env python=3.7

  - The environments created by Conda is always located in /Users/.../anaconda3/envs/  (windows)
  - 

Activate virtual environment created using conda
> conda activate my_virtualenv

Deactivating virtual environment
> conda deactivate

Install dependencies from requirements.txt using conda
> conda install pip

> pip install -r requirements.txt

List all virtual environments managed by conda
> conda env list

Display all packages in the current virtual environment
>  conda list

## Python Virtual Environment Management

pipfile

virtualenv

venv


