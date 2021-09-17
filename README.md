
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

  - tidy versions of common structures used by the Australian Bureau of
    Statistics (ABS), like ANZSIC and ANZSCO:

  - a function to tidy up state names (`clean_states()`); and

  - a function that knows whether particular dates are public holidays
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

Current structures stored in `strayr` are:

  - `anzsco2009`: occupation levels of the [Australian and New Zealand
    Standard Classification of Occupations (ANZSCO), First Edition,
    Revision 1, 2009. Cat.
    1220.0](https://www.abs.gov.au/AUSSTATS/abs@.nsf/DetailsPage/1220.0First%20Edition,%20Revision%201?OpenDocument).
  - `anzsic2006`: industry levels of the [Australian and New Zealand
    Standard Industrial Classification (ANZSIC), 2006 (Revision 1.0).
    Cat.
    1292.0](https://www.abs.gov.au/ausstats/abs@.nsf/0/20C5B5A4F46DF95BCA25711F00146D75?opendocument).
  - `asced_foe2001`: field of education levels of the [Australian Standard
    Classification of Education (ASCED), 2001. Cat.
    1272.0](https://www.abs.gov.au/ausstats/abs@.nsf/mf/1272.0).
  - `asced_qual2001`: qualification levels of the [Australian Standard
    Classification of Education (ASCED), 2001. Cat.
    1272.0](https://www.abs.gov.au/ausstats/abs@.nsf/mf/1272.0).

The `strayr` package also loads
[`absmapsdata`](https://github.com/wfmackey/absmapsdata), which contains
the following structures *and their geometry* as `sf` objects:

**ASGS Main Structures**

  - `sa12011`: Statistical Area 1 2011
  - `sa12016`: Statistical Area 1 2016
  - `sa22011`: Statistical Area 2 2011
  - `sa22016`: Statistical Area 2 2016
  - `sa32011`: Statistical Area 3 2011
  - `sa32016`: Statistical Area 3 2016
  - `sa42011`: Statistical Area 4 2011
  - `sa42016`: Statistical Area 4 2016
  - `gcc2011`: Greater Capital Cities 2011
  - `gcc2016`: Greater Capital Cities 2016
  - `ra2011`: Remoteness Areas 2011
  - `ra2016`: Remoteness Areas 2016
  - `state2011`: State 2011
  - `state2016`: State 2016

**ASGS Non-ABS Structures**

  - `ced2018`: Commonwealth Electoral Divisions 2018
  - `sed2018`: State Electoral Divisions 2018
  - `lga2016`: Local Government Areas 2016
  - `lga2018`: Local Government Areas 2018
  - `regional_ivi2008`: Regions for the Internet Vacancy Index 2008
  - `postcodes2016`: Postcodes 2016
  - `dz2011`: Census of Population and Housing Destination Zones 2011
  - `dz2016`: Census of Population and Housing Destination Zones 2016

## Converting state names and abbreviations

The `clean_state()` function makes it easy to wrangle vectors of State
names and abbreviations - which might be in different forms and possibly
misspelled.

## Australian public holidays

This package includes the `auholidays` dataset from the [Australian
Public Holidays Dates Machine Readable
Dataset](https://data.gov.au/data/dataset/australian-holidays-machine-readable-dataset)
as well as a helper function `is_holiday`:

## Parsing income ranges

The `parse_income_range` function provides some tools for extracting
numbers from income ranges commonly used in Australian data. For
example:

``` r

parse_income_range("$1-$199 ($1-$10,399)", limit = "lower")
#> [1] 1
```
