# machine-learning

This repo will run a DistilBERT model on data, while having the data tracked using dvc (data version control)

## Themes, technologies and packages used
- Model: Transformers (DistilBERT)
- Packages: poetry, dvc
- Data Science: preprocessing and predictions on data

## Set up
1. How this repo was set up to use poetry
- Poetry was installed by following the doc found on the official webiste [here](https://python-poetry.org/docs/#installing-with-the-official-installer)
- Once the installation is complete, it will ask you to add an `export PATH...` line to your shell profile. Do that.
- run the following command to activate peetry across your system `poetry config virtualenvs.in-project true`
- in your repo run `poetry init` to initialise the repo for using poetry
- run `poetry shell` to activate the poetry virtual environment. (to deactivate, run `exit`)

2. Installing dvc (data version control)
- run `poetry add dvc` when the poetry virtual environment was active.
- run `dvc init` in the repo to initialise the use of dvc within the repo.
- (optional) set up the dvc storage using `dvc remote add -d myremote s3://your-bucket-name`
- add files to be tracked by dvc `dvc add path/to/datafile_or_directory`
- commit the changes to github
- push to dvc if you set it up using `dvc push`
- push code to github
- collaborators can pull the repo and data using `git clone <repo-url>` `dvc pull`

##  Dataset used is Customer Personality Analysis dataset
It can be found here: https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis 