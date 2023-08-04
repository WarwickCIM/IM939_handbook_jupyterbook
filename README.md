[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/WarwickCIM/IM939_handbook/main)

# Data Science Across Disciplines' handbook

This repository contains the labs' handbook for [IM939: Data Science Across Disciplines](https://cagatayturkay.github.io/data-science-across-disciplines), created by Carlos Cámara-Menoyo, Cagatay Turkay and James Tripp.

![IM939 Logo](IM939_logo.png)

## Handbook

The handbook uses [jupyter-book](https://jupyterbook.org/en/stable/intro.html).

Publishing book to github pages:

```
ghp-import -n -p -f _build/html
```


## Virtual environments

Virtual environments are a way to install all the dependencies (and their right version) required for a certain project by isolating python and libraries' specific versions. Every person who recreatesthe virtual environment will be using the same packages and versions, reducing errors and increasing reproducibility.

In this project, virtual environments are managed by `conda`, which means that you should have [Anaconda distribution](https://www.anaconda.com) installed (Read [installing instructions on their website](https://www.anaconda.com/distribution/))

**Activate virtual environment**

```
conda activate env/
```

or, if  it is stored in `env/` folder:

```
conda activate env/
```

**Deactivate virtual environment:**

```
conda deactivate
```

**Update virtual environment from  `environment.yml`:**

```
conda env update -f environment.yml
```

**Recreate virtual environment from `environment.yml`:**

```
conda env create -f environment.yml
```

or, if we want to install the environment within the project:

```
conda env create --prefix env -f environment.yml
```

**Freeze used dependencies into a file**

We can create a file (in this case `environment.yml`) containing the exact libraries and versions used in the current environment. This can be useful to update the versions used in the environment in the future.

```
conda env export > environment.yml
```