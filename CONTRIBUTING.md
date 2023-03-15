# Development Setup

## Setup
To contribute to this repository, you need to ensure you have available:
- [ ] git
- [ ] conda

## Clone with git
You can clone the repository with SSH or HTTPS. For SSH, you first need to setup [SSH keys](https://docs.gitlab.com/ee/user/ssh.html) to communicate with Gitlab.
```
# HTTPS
$ git clone https://github.com/GoncaloJardim/python-academy
```

You don't need to be git-proficient to run this repo, but it may help to check a couple of git tutorials if you want to contribute ([git-guide](https://rogerdudler.github.io/git-guide/), [git-tutorial](https://backlog.com/git-tutorial/))

## Create environment with conda
1. Create the environment from the `environment.yml`file that specifies the dependencies with 
```$ conda env create -f environment.yml```


1. Activate the new environment with `conda activate python-academy`


For more details, check the original [Conda docs](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file).

## Updating the conda environment
If you need to change your package dependecies, you can update the `environment.yml` file and update the conda environment.

```bash
# option 1
conda activate python-academy
conda env update --file environment.yml --prune

# option 2
conda env update --name python-academy --file environment.yml --prune
```

## Specify specific conda channels
You can specify a specific conda channel with the syntax `{conda_channel}::{package}`.

```yml
name: python-academy
dependencies:
  - conda-forge::typeguard
```

## Run the Notebooks with JupyterLab
To run the notebooks, you can either 
1. start JupyterLab service from the active conda environment 
```
# Option 1
$ conda activate python-academy
$ jupyter lab 
```
2. Open the notebook in VSCode and select the appropriate kernel ('Select Kernel' option on top right).