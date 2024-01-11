# cran-comments.md

## Version 1.0.2

Bugfix:
- Solve bug of predicting future value that predicts an extra sample.

## donttest{} examples

Most of the functions trains a LSTM model, which requires several minutes. 
However, the donttest{} examples have been checked in the test environments.

## Test environments
All checks passed in:
* Windows 10 Home x64, R 4.3.2
* Ubuntu Linux 20.04.1 LTS, R-release, GCC (r-hub)
* Fedora Linux, R-devel, clang, gfortran (r-hub)
* win-builder, R (oldrelease, release and devel)

── R CMD check results ─────────────────────────────── TSLSTMplus 1.0.0 ────
Duration: 3m 17.7s

0 errors ✔ | 0 warnings ✔ | 0 notes ✔ 


## Downstream Dependencies
There are currently no downstream dependencies for this package.
