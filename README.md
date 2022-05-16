
<!-- README.md is generated from README.Rmd. Please edit that file -->

# foofactors

<!-- badges: start -->
<!-- badges: end -->

The goal of foofactors is to separate a string, but to prevent R from
making it a list.

## Installation

You can install the development version of foofactors from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("LaurineSeelt/foofactors")
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r
# install.packages("devtools")
devtools::install_github("LaurineSeelt/foofactors")
#> Skipping install of 'foofactors' from a github remote, the SHA1 (6b2902e7) has not changed since last install.
#>   Use `force = TRUE` to force installation
library(foofactors)
(x <- "alfa,bravo,charlie,delta")
#> [1] "alfa,bravo,charlie,delta"
str_split_one(x, pattern = ",")
#> [1] "alfa"    "bravo"   "charlie" "delta"
```

<br> This works better than the example below. <br>

``` r
(x <- "alfa,bravo,charlie,delta")
#> [1] "alfa,bravo,charlie,delta"
strsplit(x, split = ",")
#> [[1]]
#> [1] "alfa"    "bravo"   "charlie" "delta"
stringr::str_split(x, pattern = ",")
#> [[1]]
#> [1] "alfa"    "bravo"   "charlie" "delta"
```

<br> This returns a list of 1. Thus output is often inconvenient, so the
foofactors function solves this.
