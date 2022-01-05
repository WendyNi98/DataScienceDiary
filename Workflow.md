# Data Science Project Workflow for Production

## Content
### 1. Virtual Environment
### 2. Version Control with Git
### 3. Coding Convention and Tips
#### 3.1 Code Style
#### 3.2 Refactor
### 4. Production
#### 4.1 Custom Exception
#### 4.2 Testing
### 5. Handover
#### 5.1 Documentation
### Appendix: Code Base


# 1. Virtual Environment

Using virtual environment is essential and has following benefits:
- Allows stable rerun of the programme
- Minimize impact of change in environment
- Saves time for debugging

Anaconda can easily create and manage virtual environments, either using GUI or command line.

Create virtual environment:

```
conda create -n <venv-name> python=3.8
```

Activate virtual environment:

```
activate <venv-name>
```

List virtual environments:

```
conda env list
```

Add created virtual environment to Jupyter Notebook (for EDA):

```
pip install ipykernel
ipython kernel install --user --name=<venv-name>
```

Find more commands at [Anaconda Cheatsheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf)

Generate requirements.txt:

```
pip freeze > requirements.txt
```


# 2. Version Control with Git

Version control makes it easy to collaborate and revert changes.

New git repository: 

```
git init
```

Add new files:

```
git add
```

Commit:

```
git commit -am "<commit-message>"
```

Find more details in [Git Tutorial](https://www.atlassian.com/git/tutorials)

# 3. Coding Convention and Tips
### 3.1 Code Style

[PEP8](https://www.python.org/dev/peps/pep-0008/)
[BOBP Guide for Python](https://gist.github.com/sloria/7001839)

### 3.2 Refactor

Refactor often to improve efficiency.  
Limit use of hardcode and use config.

[Production Data Science](https://github.com/FilippoBovo/production-data-science)


# 4. Production
## 4.1 Custom Exception

Use custom exceptions to prevent interruption due to error in production and identify bugs quickly. 

```
Class CustomException():
    pass
try:
    pass
except CustomException:
```

[Python Exception Documentation](https://docs.python.org/3/tutorial/errors.html)

## 4.2 Testing

Constant testing to facilitate integration.

[Pytest Documentation](https://docs.pytest.org/en/6.2.x/)

# 5. Handover
## 5.1 Documentation

Documentation should include:
- Methodology
- Maintenance guide


# Appendix: Code Base
### I. EDA
pandas-profiling  
Visualization  
Tests  

### II. Util Functions
Timing  
Logging  
Exception  

### III. Templates
File Structure [cookiecutter](https://cookiecutter.readthedocs.io/en/1.7.2/README.html)
Documentation Template
