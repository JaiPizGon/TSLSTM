# cran-comments.md

## Version 1.0.6

Add lagmatrix function in package to avoid dependency of smooth package through
the ts.utils package. This function might be deprecated in future releases
once ts.utils package updates its dependencies.

## donttest{} examples

Most of the functions trains a LSTM model, which requires several minutes. 
However, the donttest{} examples have been checked in the test environments.

## Test environments
All checks passed in all platforms provided by rhub::rc_submit(), which includes 
Windows, Linux and MacOS.

── R CMD check results ────────────────────────────────────────────────────────────────────────────────── TSLSTMplus 1.0.5 ────
Duration: 1m 48.2s

❯ checking for future file timestamps ... NOTE
  unable to verify current time

0 errors ✔ | 0 warnings ✔ | 1 note ✖

This note seems to be due to http://worldclockapi.com/ not being available, which 
is used by check() to verify the current time. This is not a problem with the package.

## Downstream Dependencies
There are currently no downstream dependencies for this package.
