# Agile Data Science Cookiecutter Template

_A minial and flexible project structure for data science projects._


### Requirements to use the cookiecutter template:
-----------
 - Python 2.7 or 3.5
 - [Cookiecutter Python package](http://cookiecutter.readthedocs.org/en/latest/installation.html) >= 1.4.0: This can be installed with pip by or conda depending on how you manage your Python packages:

``` bash
$ pip install cookiecutter
```

or

``` bash
$ conda config --add channels conda-forge
$ conda install cookiecutter
```


### To start a new project, run:
------------

    cookiecutter https://github.com/


### The resulting directory structure
------------

The directory structure of your new project looks like this: 

```
│   README.md
|
|───data/
|   │___raw/
|   │___cache/
|
|───reports/
|   |___report_xx/
|       |___plots/
|       |___code/
|
|___code/
|   |___utils/
|   |___eda/
|   |___diagnostics/
|
|___docs/
|
|___tests/
|
```

### Installing development requirements
------------

    pip install -r requirements.txt


### testing environment
------------

    python test_environment.py


