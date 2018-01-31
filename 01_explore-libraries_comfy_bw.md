01\_explore-libraries\_comfy\_bw.R
================
Brian Wozniak
Wed Jan 31 14:06:00 2018

Which libraries does R search for packages?

``` r
# try .libPaths(), .Library
.libPaths()
```

    ## [1] "C:/Users/Brian Wozniak/Documents/R/win-library/3.4"
    ## [2] "C:/Program Files/R/R-3.4.3/library"

``` r
.Library
```

    ## [1] "C:/PROGRA~1/R/R-34~1.3/library"

Installed packages

``` r
## use installed.packages() to get all installed packages
## if you like working with data frame or tibble, make it so right away!
## remember to use View() or similar to inspect

pack <- data.frame(installed.packages())
## how many packages?
195
```

    ## [1] 195

Exploring the packages

``` r
## count some things! inspiration
##   * tabulate by LibPath, Priority, or both
##   * what proportion need compilation?
##   * how break down re: version of R they were built on

## for tidyverts, here are some useful patterns
# data %>% count(var)
# data %>% count(var1, var2)
# data %>% count(var) %>% mutate(prop = n / sum(n))
```

Reflections

``` r
## reflect on ^^ and make a few notes to yourself; inspiration
##   * does the number of base + recommended packages make sense to you?
##   * how does the result of .libPaths() relate to the result of .Library?
```

Going further

``` r
## if you have time to do more ...

## is every package in .Library either base or recommended?
## study package naming style (all lower case, contains '.', etc
## use `fields` argument to installed.packages() to get more info and use it!
```
