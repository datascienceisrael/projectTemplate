# Agile Data Science Cookiecutter Template

_A minial and flexible project structure for data science projects._


### Requirements to use the cookiecutter template:
-----------
 - Python (!)
 - [Cookiecutter Python package](http://cookiecutter.readthedocs.org/en/latest/installation.html) >= 1.4.0: This can be installed with pip by or conda depending on how you manage your Python packages:

``` bash
$ pip install cookiecutter
```

or

``` bash
$ conda config --add channels conda-forge
$ conda install cookiecutter
```


### Start a new Data Science project:
============

```bash
$ cookiecutter https://github.com/datascienceisrael/projectTemplate.git
```

### The resulting directory structure

The new project will be structured like this: 

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

Two additional files are created in the new project:

 + **requirements.txt**  
 + **test_environment.py**

The requirements file holds common data science python modules.
Installation of these modules is done with:

```bash
$ pip install -r requirements.txt
```

test_enviroment is used to make sure you are using the correct python version with  
this project. 
Run test with:

```bash
$ python test_environment.py
```

