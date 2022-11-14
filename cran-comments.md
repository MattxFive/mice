cran-comments
================

## mice 3.15.0

New submission.

## Reason

`mice 3.15.0` contains many changes and enhancements over `mice 3.14.0`

## Test environments

### Local

``` r
R.Version()
```

    ## $platform
    ## [1] "aarch64-apple-darwin20"
    ## 
    ## $arch
    ## [1] "aarch64"
    ## 
    ## $os
    ## [1] "darwin20"
    ## 
    ## $system
    ## [1] "aarch64, darwin20"
    ## 
    ## $status
    ## [1] ""
    ## 
    ## $major
    ## [1] "4"
    ## 
    ## $minor
    ## [1] "2.1"
    ## 
    ## $year
    ## [1] "2022"
    ## 
    ## $month
    ## [1] "06"
    ## 
    ## $day
    ## [1] "23"
    ## 
    ## $`svn rev`
    ## [1] "82513"
    ## 
    ## $language
    ## [1] "R"
    ## 
    ## $version.string
    ## [1] "R version 4.2.1 (2022-06-23)"
    ## 
    ## $nickname
    ## [1] "Funny-Looking Kid"

### win-builder

### \* Rhub

## Local check

Package built by

``` r
library("devtools")
build()
```

``` bash
R CMD CHECK mice_3.14.12.tar.gz
```

Status: OK

## win-builder

``` r
devtools::check_win_devel()
```

Status: 2 NOTES

## Rhub checks

``` r
devtools::check_rhub()
```

Results:

1.  Debian Linux, R-devel, GCC ASAN/UBSAN:
2.  Windows Server 2022, R-devel, 64 bit: **Success**
3.  Ubuntu Linux 20.04.1 LTS, R-release, GCC:
4.  Fedora Linux, R-devel, clang, gfortran:

## Downstream dependencies

I have run

``` r
library(revdepcheck)
revdep_reset()
revdep_check(num_workers = 10)
```

### `failures.md`

There is one old failure (`dynr`):
`configure: error: gsl-config not found, is GSL installed?` Not related
to `mice`.

### `problems.md`

    # CALIBERrfimpute

    <details>

    * Version: 1.0-5
    * GitHub: NA
    * Source code: https://github.com/cran/CALIBERrfimpute
    * Date/Publication: 2021-05-05 09:00:04
    * Number of recursive dependencies: 53

    Run `revdep_details(, "CALIBERrfimpute")` for more info

    </details>

    ## Newly broken

    *   checking running R code from vignettes ...
          ‘simstudy_survival.Rnw’ using ‘UTF-8’... failed
         ERROR
        Errors in running code in vignettes:
        when running code in ‘simstudy_survival.Rnw’
          ...
          x2 & 0.0391  & 0.0254  & 0.0138  \\ 
          x3 & -0.0314  & -0.00854  & -0.0228  \\ 
           \hline
        \end{tabular}
        
        \vspace{1em}
        
          When sourcing ‘simstudy_survival.R’:
        Error: missing value where TRUE/FALSE needed
        Execution halted

Not sure whether it’s related to `mice`, and seems relatively benign if
it is. The package maintainer of `CALIBERrfimpute` is aware of the
problem, and will look into the issue.
