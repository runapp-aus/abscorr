
<!-- README.md is generated from README.Rmd. Please edit that file -->

# strayr <img src="man/figures/apple-touch-icon-152x152.png" align="right" style="height:150px"/>

<!-- badges: start -->

[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
[![R build
status](https://github.com/runapp-aus/strayr/workflows/R-CMD-check/badge.svg)](https://github.com/runapp-aus/strayr/actions)

<!-- badges: end -->

The `strayr` package provides tools to make working with Australian data
easier. This includes:

-   tidy versions of common structures used by the Australian Bureau of
    Statistics (ABS), like ANZSIC and ANZSCO:

-   a function to tidy up state names (`clean_states()`); and

-   a function that knows whether particular dates are public holidays
    (`is_holiday()`).

This package is currently **in development** and subject to change. The
lifecycle badge will be changed to `stable` when it is stable (should be
relatively soon).

**Contribute to this package**: people are actively encouraged to
contribute to this package.

## Installation

You can install the current version of `strayr` with:

``` r
remotes::install_github("runapp-aus/strayr")
```

## Structures
