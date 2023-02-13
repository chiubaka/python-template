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
3. Install `pre-commit` hooks: `poetry run pre-commit install --hook-type pre-commit --hook-type pre-push`

#### Linting and Formatting Integration with VS Code
VS Code can be configured to highlight linting errors and help you reformat
code to conform to style guidelines.

1. Open VS Code's settings (Command + , on macOS)
2. Search for `flake8`
3. Check the box under `Python > Linting: Flake8 Enabled`
    1. If prompted to install `flake8`, go ahead and do so. This installs `flake8` globally, and is separate from `poetry`'s installed `flake8` binary.
4. Search again for `black` in settings
5. Under `Python > Formatting: Provider`, select `black` from the dropdown menu

### Workflows
- To run the project: `poetry run python python_template/main.py`
- To lint the project: `poetry run flake8`
- To auto-format the project: `poetry run black .`
- To run tests: `poetry run pytest`
