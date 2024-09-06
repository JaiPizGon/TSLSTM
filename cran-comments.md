# cran-comments.md

## Version 1.0.5

Bugfix:
- Solve bug if xreg is only one variable and scaler is used.

## donttest{} examples

Most of the functions trains a LSTM model, which requires several minutes. 
However, the donttest{} examples have been checked in the test environments.

## Test environments
All checks passed in:
* Windows 11 Home x64, R 4.3.3
* Ubuntu Linux 20.04.1 LTS, R-release, GCC (r-hub)
* Fedora Linux, R-devel, clang, gfortran (r-hub)
* win-builder, R (oldrelease, release and devel)

── R CMD check results ─────────────────────────────── TSLSTMplus 1.0.5 ────
Duration: 3m 17.7s

0 errors ✔ | 0 warnings ✔ | 0 notes ✔ 


## Downstream Dependencies
There are currently no downstream dependencies for this package.
