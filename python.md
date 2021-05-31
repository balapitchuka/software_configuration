### Managing multiple versions of python on a machine

#### pyenv

Note: linux based os comes with default python installed based on type of os
      - If you want to install other versions use pyenv to manage them all

Install and configure pyenv

> pyenv versions

> pyenv global 3.6.5

>pyenv local 3.7.8

> pyenv virtualenv 3.6.7 env_name

> pyenv activate env_name

> pyenv deactivate


creating virtual environments for python

pipfile

virtualenv

venv


installing jupyter notebooks


#### anaconda
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



