
randquotes
==========

[![Build Status](https://travis-ci.org/amrrs/randquotes.svg?branch=master)](https://travis-ci.org/amrrs/randquotes) [![codecov](https://codecov.io/gh/amrrs/randquotes/branch/master/graph/badge.svg)](https://codecov.io/gh/amrrs/randquotes) [![CRAN status](https://www.r-pkg.org/badges/version/randquotes)](https://cran.r-project.org/package=randquotes) [![DOWNLOADSTOTAL](https://cranlogs.r-pkg.org/badges/grand-total/randquotes)](https://cranlogs.r-pkg.org/badges/grand-total/randquotes)

Description
-----------

This package connects to the site <http://quotesondesign.com/> that uses the WordPress JSON REST API to provide a way for you to grab quotes.

Overview
--------

This package contains the following function: `randquote()` that fetches a random quote and returns a dataframe along with the author name and link to the quote.

Installation
------------

The stable version of `randquotes` can be installed from CRAN:

``` r
install.packages("randquotes")
```

And the development version can be installed from github:

``` r
devtools::install_github("amrrs/randquotes")
```

### Note

This package fetches data from API hence an active internet connection is required for this package to function.

Current Version
---------------

``` r
library(randquotes)

# current verison
packageVersion("randquotes")
```

    ## [1] '0.1.0'

Usage
-----

### Get Random Quote

``` r
library(randquotes)

randquote()
```

    ##     ID        title                                                                             content
    ## 1 2356 Ralph Caplan <p>Design is a process for making things right, for shaping what people need.</p>\n
    ##                                       link
    ## 1 https://quotesondesign.com/ralph-caplan/
    ##                                                                                        Source
    ## 1 <a href="http://www.amazon.com/Design-There-Bathroom-Object-Lessons/dp/0070097771">book</a>

### Get only the Quote

Sometimes you may not be interested in getting a dataframe that has ID and link, so this function `randquote_simple()` outputs only the quote with author name.

``` r
library(randquotes)

cat(randquotes::randquote_simple())
```

    ## If we want users to like our software we should design it to behave like a likeable person: respectful, generous and helpful.  
    ## -Alan Cooper

Courtesy
--------

This R package is powered by [Quotes on Design API](https://quotesondesign.com/api-v4-0/)

Code of Conduct
---------------

Please note that this project is released with a [Contributor Code of Conduct](CONDUCT.md). By participating in this project you agree to abide by its terms.
