# Guidelines

## Respository Structure
Each repository contains at least the following folders:
- `src`: all source code
- `test`: (unit) tests for the source code, each subfolder/package should follow the same structure as in the src folder
- `doc`: documentation

## Coding guidelines
- use [PEP 8 – Style Guide for Python Code](https://peps.python.org/pep-0008/)
- Add a README.md file to every project detailing the project's goal, structure, installation and any further information you deem relevant to first time users.

### Package build
- create a `setup.py` or a `pyproject.toml` file 
  - `pyproject.toml` is preferred
  - Consistently update version numbers 
    - follow the scheme: Major.Minor.Patch
    - MAJOR version when you make incompatible API changes
    - MINOR version when you add functionality in a backward compatible manner
    - PATCH version when you make backward compatible bug fixes


## Install local dependencies
Create a virtual environment (if not yet done):
- `python -m venv /path/to/venv`

Enter your virtual environment:
- `source /path/to/venv/bin/activate`

Navigate to the folder of the required dependency and install using pip
- `pip install .`

or 
- `pip install -e .`
to install in editable mode in which changes to the source code will be immediately reflected in your Python environment, without the need to reinstall the package each time you make changes.

If PyCharm does not recognize the locally installed dependency:
- go to settings (shortcut `CTRL`+`Alt`+`s`)
- navigate to your project > project dependencies
- activate all project the chosen project depends on
