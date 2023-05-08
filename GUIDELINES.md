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
