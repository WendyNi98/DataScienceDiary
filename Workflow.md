# Data Science Project Workflow for Production

## Content
### 1. Virtual Environment
### 2. Version Control with Git
### 3. Coding Convention and Tips
#### 3.1 Refactor
### 4. Production
#### 4.1 Customize Exception
#### 4.2 Testing
### 5. Handover
#### 5.1 Documentation


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

See more commands at [Anaconda venv documentation](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf)


