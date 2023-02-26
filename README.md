# Basic package

Following the simple tutorial at:
https://www.freecodecamp.org/news/how-to-create-and-upload-your-first-python-package-to-pypi/

We use setuptools as a "build system" here. This is declared in `pyproject.toml`. 
Note that you can safely move all configuration settings in `setup.cfg` to `pyproject.toml` if you 
decide to change the build system to flit or poetry, for example.

### Usage

E.g.

    from multiply.by_three import multiply_by_three
    from divide.by_three import divide_by_three

    multiply_by_three(9)
    divide_by_three(21)

### Generate distribution archives

In the same directory as the `pyproject.toml` file, do

    python -m pip install --upgrade build
    python -m build

Once the process above is completed, a new directory is generated called dist/ with two files in it. 
The .tag.tz file is the source archive and the .whl* file is the built archive. These files 
represent the distribution archives of our Python package which will be uploaded to the Python 
Package Index and installed by pip in the following sections.


