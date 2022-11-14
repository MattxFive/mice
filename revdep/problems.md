# adjustedCurves

<details>

* Version: 0.9.0
* GitHub: https://github.com/RobinDenz1/adjustedCurves
* Source code: https://github.com/cran/adjustedCurves
* Date/Publication: 2022-09-22 08:40:13 UTC
* Number of recursive dependencies: 167

Run `revdepcheck::revdep_details(, "adjustedCurves")` for more info

</details>

## Newly broken

*   checking tests ...
    ```
      Running ‘testthat.R’
     ERROR
    Running the tests in ‘tests/testthat.R’ failed.
    Last 13 lines of output:
        5. ├─dplyr:::summarise.grouped_df(...)
        6. │ └─dplyr:::summarise_cols(.data, dplyr_quosures(...), caller_env = caller_env())
        7. │   ├─base::withCallingHandlers(...)
        8. │   └─dplyr:::map(quosures, summarise_eval_one, mask = mask)
        9. │     └─base::lapply(.x, .f, ...)
       10. │       └─dplyr (local) FUN(X[[i]], ...)
       11. │         └─mask$eval_all_summarise(quo)
       12. ├─adjustedCurves:::pool_p_values(p_val)
       13. └─base::.handleSimpleError(...)
       14.   └─dplyr (local) h(simpleError(msg, call))
       15.     └─rlang::abort(bullets, call = error_call, parent = skip_internal_condition(e))
      
      [ FAIL 7 | WARN 126 | SKIP 125 | PASS 1579 ]
      Error: Test failures
      Execution halted
    ```

# qgcomp

<details>

* Version: 2.9.0
* GitHub: https://github.com/alexpkeil1/qgcomp
* Source code: https://github.com/cran/qgcomp
* Date/Publication: 2022-10-13 08:30:07 UTC
* Number of recursive dependencies: 135

Run `revdepcheck::revdep_details(, "qgcomp")` for more info

</details>

## Newly broken

*   checking tests ...
    ```
      Running ‘test_asis.R’
      Running ‘test_basics.R’
      Running ‘test_bayesqgcomp.R’
      Running ‘test_boot_ints.R’
      Running ‘test_bootchooser.R’
      Running ‘test_factor.R’
      Running ‘test_id.R’
      Running ‘test_mice.R’
      Running ‘test_numeric.R’
      Running ‘test_poisson.R’
    ...
      +   traindata=spl$traindata,validdata=spl$validdata, expnms=Xnm)
      Error in qgcomp.noboot(expnms = c("copper", "arsenic", "sodium", "selenium",  : 
        Model aliasing occurred, likely due to perfectly correlated quantized exposures.
                 Try one of the following:
                   1) set 'bayes' to TRUE in the qgcomp function (recommended)
                   2) set 'q' to a higher value in the qgcomp function (recommended)
                   3) check correlation matrix of exposures, and drop all but one variable in each highly correlated set  (not recommended)
                 
      Calls: qgcomp.partials -> eval -> eval -> qgcomp.noboot
      Execution halted
    ```

