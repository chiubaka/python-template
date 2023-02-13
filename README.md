# python-template
A sample Python template project equipped with modern tooling for development.

## Local Development

### Setup
1. You need `poetry` installed to work with this repository.
  1. Follow the installation instructions [here](https://python-poetry.org/docs/#installation).
  2. Make sure you add `poetry` to your path by adding the following line to the bottom of your `~/.bashrc` or `~/.bash_profile` file (choose whichever already exists): `export PATH="/Users/dchiu/.local/bin:$PATH"`
  3. Open a new Terminal window and check that `poetry` is installed by running `poetry --version`. You should see a version number printed to the console (if you see `command not found`, `poetry` was not installed correctly).
    1. Opening a new Terminal window reloads `bash` with new settings required to find `poetry`.
2. Once you have `poetry` installed, run `poetry install` in the project root to install all project dependencies.
3. Install `pre-commit` hooks: `poetry run pre-commit install`

### Workflows
- To run the project: `poetry run python python_template/main.py`
- To lint the project: `poetry run flake8`
- To auto-format the project: `poetry run black .`
- To run tests: `poetry run pytest`
