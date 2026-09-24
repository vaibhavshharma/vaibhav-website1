# Personal Quarto Website

This repository contains my personal Quarto website, including computational blog posts written in Python and R.

## Prerequisites

This website was built using:

- Quarto 1.10.18
- uv 0.12.7
- R 4.6.1

The R package `renv` will bootstrap the R environment from the lockfile.

## Clone the repository

In a terminal, run:

```bash
git clone https://github.com/vaibhavshharma/vaibhav-website1.git
cd vaibhav-website1
```

## Python environment

From the project root, restore the Python environment:

```bash
uv sync
```

The Python environment is defined by `pyproject.toml` and `uv.lock`.

## R environment

From the project root, start R:

```bash
R
```

Then, at the R prompt, restore the R dependencies:

```r
renv::restore()
```

After the restore finishes, exit R:

```r
q()
```

## Build the website

From the project root, run:

```bash
uv run quarto render
```

The rendered website is generated in the `_site/` directory.

To view the website locally, run:

```bash
uv run quarto preview
```

Then open the local address displayed by Quarto in your web browser.

## Data

The computational blog posts use the Palmer Penguins dataset from the `palmerpenguins` package.

The dataset is provided through the installed package, so the build does not need to download a separate data file. An internet connection is required when initially installing/restoring the project dependencies.