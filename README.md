pyautomagic
==============================
[![Coverage Status](./coverage.svg)](./coverage.svg)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/ambv/black)
![GitHub](https://img.shields.io/github/license/NeuroDataDesign/pyautomagic)
![PyPI](https://img.shields.io/pypi/v/pyautomagic)
![GitHub last commit](https://img.shields.io/github/last-commit/NeuroDataDesign/pyautomagic)
![GitHub repo size](https://img.shields.io/github/repo-size/NeuroDataDesign/pyautomagic)

A Python3 version of the automagic EEG processing pipeline. Development in progress. This is all temporary.

References
----------
1. Paper: https://www.biorxiv.org/content/10.1101/460469v1
2. Paper: https://www.ncbi.nlm.nih.gov/pubmed/31233907
3. Matlab github repo: https://github.com/methlabUZH/automagic


Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── pyautomagic
    |   ├── src            <- Src/ from automagic (matlab)
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── base           <- Scripts that are configuration files, or other code used by the entire pyautomagic repo.
    │   │
    │   ├── gui             <- Scripts for the gui
    │   │
    │   ├── preprocessing   <- Scripts for running EEG preprocessing
    │   │
    │   └── visualization  <- Scripts to visualize results, etc.
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.testrun.org


--------


## Intended Users / Usage

Researchers dealing with EEG data. The main (default) workflow is summarized in: 

# Installation Guide
pyautomagic relies on the following libraries to work:

    numpy
    scipy
    scikit-learn
    pandas
    mne
    
Setup environment via Conda:


    conda create -n pyautomagic
    conda activate pyautomagic
    conda config --add channels conda-forge
    conda install numpy pandas mne scipy scikit-learn seaborn
    
## Install from Github
To install, run this command in your repo:

    pip install -e git+https://github.com/NeuroDataDesign/pyautomagic#egg=pyautomagic

# Documentation
Use sphinx to generate documentation:

    sphinx-quickstart
    

# Testing
Run tests and also autoformatting of your code. Install black, pylint, pytest, and pytest-coverage.

    black eegio/*
    pylint ./eegio/
    pytest --cov-config=.coveragerc --cov=./eegio/ tests/
    coverage-badge -f -o coverage.svg

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>