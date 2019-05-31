
<!-- README.md is generated from README.Rmd. Please edit that file -->

# startrek <img src="man/figures/logo.png" align="right" height=150/>

<!-- badges: start -->

[![Travis build
status](https://travis-ci.org/tyluRp/startrek.svg?branch=master)](https://travis-ci.org/tyluRp/startrek)
[![AppVeyor build
status](https://ci.appveyor.com/api/projects/status/github/tyluRp/startrek?branch=master&svg=true)](https://ci.appveyor.com/project/tyluRp/startrek)
<!-- badges: end -->

The goal of startrek is to access Star Trek transcripts in a
[`data.frame`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/data.frame.html)
for easy analysis. All transcripts have been parsed from text files to a
[tidy data](http://vita.had.co.nz/papers/tidy-data.html) format.

## Installation

You can install the development version from GitHub:

``` r
devtools::install_github("tylurp/startrek")
```

Or, just download the data to disk from the data folder in this
repository.

## Example

To access an episode transcript from The Next Generation series, see the
`tng` list:

``` r
library(startrek)
library(tibble)

as_tibble(tng$`The Inner Light`)
#> # A tibble: 410 x 5
#>    perspective     setting            character description line           
#>    <chr>           <chr>              <chr>     <chr>       <chr>          
#>  1 3 EXT. SPACE -… at warp.           PICARD (… <NA>        Captain's log,…
#>  2 4 INT. BRIDGE   PICARD, RIKER, DA… PICARD    <NA>        The last time …
#>  3 4 INT. BRIDGE   PICARD, RIKER, DA… GEORDI    <NA>        Nine hours... ?
#>  4 4 INT. BRIDGE   PICARD, RIKER, DA… PICARD    <NA>        "The entire \"…
#>  5 4 INT. BRIDGE   PICARD, RIKER, DA… RIKER     <NA>        That's a littl…
#>  6 4 INT. BRIDGE   PICARD, RIKER, DA… PICARD    <NA>        And for me... …
#>  7 4 CONTINUED:    PICARD, RIKER, DA… WORF      <NA>        Sir, sensors d…
#>  8 4 CONTINUED:    PICARD, RIKER, DA… PICARD    <NA>        On screen.     
#>  9 5 ANGLE - VIEW… An alien object o… PICARD    <NA>        Magnify.       
#> 10 5 ANGLE - VIEW… The object spring… PICARD    <NA>        Mister Data?   
#> # … with 400 more rows
```
