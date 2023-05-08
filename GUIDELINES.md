# Guidelines

## Respository Structure
Each repository contains at least the following folders:
- `src`: all source code
- `test`: (unit) tests for the source code, each subfolder/package should follow the same structure as in the src folder
- `doc`: documentation

## Coding guidelines
- use [PEP 8 – Style Guide for Python Code](https://peps.python.org/pep-0008/)
- bump version number in setup.py and README.md after changes
  - Version numbers follow the scheme: Major.Minor.Patch

## Install local dependencies
Enter your virtual environment:
- `source venv/bin/activate`

Navigate to the folder of the required dependency and build it
- `python3 setup.py bdist_wheel`

Then install using pip:
- e.g. `pip install ./dist/OpenDSSWrapper-0.1.1-py3-none-any.whl` (adjust project name and version number)

### Development
During development `pip install -e .` is sufficient.
`pip install -e .` is a command that installs a Python package in "editable mode" (also known as "develop mode" or "in-place installation"). The -e flag stands for "editable". When you run this command, pip will install the package in such a way that any changes you make to the package's source code will be immediately reflected in your Python environment, without the need to reinstall the package each time you make changes.
