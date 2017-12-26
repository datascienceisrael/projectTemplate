# Agile Data Science Project Template

_A minial and flexible project structure for data science projects._


Table of Contents
=================

 * [Requirements to use the cookiecutter template](#requirements-to-use-the-cookiecutter-template)
 * [Starting a new Data Science project](#starting-a-new-data-science-project)
 * [Managing Large Projects](#managing-large-projects)
 * [Github Integration](#github-integration)
 * [Additional Resources](#additional-resources)

<br>

### Requirements to use the cookiecutter template

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

<br>

### Starting a new Data Science project

To generate a Data Science project template, in your bash, run:

```bash
$ cookiecutter https://github.com/datascienceisrael/projectTemplate.git
```


The resulting directory structure for the new project will be: 

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
|───code/
|   |___utils/
|   |___eda/
|   |___diagnostics/
|
|───docs/
|
|───tests/
|
|───assets/
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

test_environment is used to make sure you are using the correct python version with  
this project. 
Run test with:

```bash
$ python test_environment.py
```

<br>


### Managing Large Projects

Big scale projects can be thought of in terms of hypotheses.  
For example, a lengthy data project called *BIG_DATA* can be divided into the following series of hypotheses:

<br>
    
  + **Data Exploration (1st hypothesis)**
    + Integrity checks
    + Features Distributions
    + Correlations
    + Time dependencies  

    <br>    
    
  + **Dimensionality Reduction (2nd hypothesis)**
    + PCA and Factor Analysis
    + Clustering
    + word2vec embedding  
    
    <br>
    
  + **Modelling (3rd hypothesis)**
    + Benchmark models
    + Hyper-parameter optimized models
    + Ensembles

<br>

Each hypothesis is treated as a mini-project,  
and each mini-project is built upon the structure induced by cookiecutter.

Hence, the structure of project *BIG_DATA* will be:


```

|   README.md
| 
|───Data Exploration
|      |
|      │   README.md
|      |
|      |───data/
|      |   │___raw/
|      |   │___cache/
|      |
|      |───reports/
|      |   |___report_xx/
|      |       |___plots/
|      |       |___code/
|      |
|      |───code/
|      |   |___utils/
|      |   |___eda/
|      |   |___diagnostics/
|      |
|      |───docs/
|      |
|      |───tests/
|      |
|      |___assets/
| 
|───Dimensionality Reduction
|      |
|      │   README.md
|      |
|      |───data/
|      |   │___raw/
|      |   │___cache/
|      |
|      |───reports/
|      |   |___report_xx/
|      |       |___plots/
|      |       |___code/
|      |
|      |───code/
|      |   |___utils/
|      |   |___eda/
|      |   |___diagnostics/
|      |
|      |───docs/
|      |
|      |───tests/
|      |
|      |___assets/
|
...
```


<br>


### Github Integration

**Every new project should be hosted on github *first*.**

The first thing to do before executing _cookiecutter_ is to create a github repository to host the project.

Once the repository is created on Github, select a working directory to store the project locally.
For example:

```bash
$ cd myProjects
```
Then, use cookiecutter to generate the project template with:

```bash
$ cookiecutter https://github.com/datascienceisrael/projectTemplate.git
```
You will be prompted to enter 

  + project_name    
  + repo_name       (this is the name of the newly created directory)
  + author
  + description
  + license 
  
Once done, you will see a new local directory *repo_name* with the appropriate files and folders.


The next step is to integrate this folder with the remote Github repository.  

Use this series of bash commands:

```bash
$ cd repo_name
$ git init

# Add the files in the local repository and stage them for commit
$ git add . 

# Commit the tracked changes and prepare them to be pushed to a remote repository
$ git commit -m "Initial commit" 

# track the new remote - the new repository you just hosted on Github
$ git remote add origin remote repository URL 
$ git push origin master
```

All done!

You should have an updated repository on Github.


<br>


### Additional Resources


  * This project supplements the basics of **Github repository structure** covered in `agileDataScience` repository - this is your goto link if you are uncertain of the contents for each folder


  * Read more about [cookiecutter](http://cookiecutter.readthedocs.io/en/latest/first_steps.html)
  
