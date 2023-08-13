# POETRY setup
**Reference**: [Poetry CLI](https://python-poetry.org/docs/cli/)

## Install pipx for global CLI availability
**Reference**: [pipx-in-pipx](https://pypi.org/project/pipx-in-pipx/)
> pip install pipx-in-pipx

## Install Poetry
Install using pipx to have the CLI available globally
> pipx install poetry

## Poetry: Create virtualenv inside project
Make poetry to install virtualenvs inside project folder
> poetry config virtualenvs.in-project true

# POETRY Management

## Setup Poetry project
Setup Poetry project using the below command  
Provide the required details asked by poetry CLI to create pyproject.toml file
> poetry init

## Create or Activate virtual environment
Virtual environment will also get activated by default while running other commands like 'poetry install'
> poetry shell

## Install dependencies
Install all dependencies
> poetry install

Install with groups
> poetry install with dev

Sync environment with lock file
> poetry install --sync

## Update depenedencies
Update all dependencies
> poetry update

Update specific dependencies
> poetry update requests toml

## Install new dependencies
### Install latest version
> poetry add requests pendulum

### Install and allow minor version update  
Allow >=2.0.5, <3.0.0 versions
> poetry add pendulum@^2.0.5

### Install and allow bugfix version update  
Allow >=2.0.5, <2.1.0 versions
> poetry add pendulum@~2.0.5

### Install without upperbound  
Allow >=2.0.5 versions, without upper bound
> poetry add "pendulum>=2.0.5"

### Install only specified version  
Allow only 2.0.5 version
> poetry add pendulum==2.0.5

### Add git dependency
> poetry add git+https://github.com/sdispater/pendulum.git

### Add local dependency
> poetry add ../my-package/dist/my_package-0.1.0.whl

### Add dependency to a group
The below command will add pytest to dev dependencies
> poetry add pytest -G dev

## Uninstall dependencies
### Uninstall a dependency
> poetry remove pendulum

### Uninstall a dependency from a specific group
> poetry remove pytest --group dev

## List dependencies
### List all dependencies
> poetry show

### List specific dependency
> poetry show pendulum

## Build Project
> poetry build

## Publish Project
> poetry publish
