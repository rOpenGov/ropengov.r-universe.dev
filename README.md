# rOpenGov setup for the r-universe

This repository holds a `packages.json` files
with the packages to be included in the dedicated universe 
[ropengov.r-universe.dev/](https://ropengov.r-universe.dev)


rOpenGov r-universe project: <https://github.com/orgs/ropengov/projects>

Source universe for ropengov: <https://github.com/r-universe/ropengov>

Last deployment: <https://ropengov.r-universe.dev>

## Adding a new package to the r-universe

Just commit to [packages.json](https://github.com/rOpenGov/universe/blob/master/packages.json) with the following information:

```json

[
  ...
  },

  {
    "package": "name_of_the_package",
    "url": "https://url_of_the_repo",
    "branch" : "optional: name_of_the_branch e.g main",
    "subdir": "optional: name_of_the_subdir"
  },
  
  ...
  
  {
    "package": "hetu",
    "url": "https://github.com/rOpenGov/hetu"
  }
]
```

In a few minutes it would be available on 
<https://ropengov.r-universe.dev>.  

## Usage

```r

# Enable this universe
options(repos = c(
    ropengov = 'https://ropengov.r-universe.dev',
    CRAN = 'https://cloud.r-project.org'))

# Install some packages
install.packages('eurostat')

```

