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


### Starting a new Data Science project:
-----------

To generate a Data Science project template, in your bash, run:

```bash
$ cookiecutter https://github.com/datascienceisrael/projectTemplate.git
```

#### Resulting directory structure

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


