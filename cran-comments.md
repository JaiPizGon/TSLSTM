# cran-comments.md

## Reviewer comments

- **Please reduce the length of the title to less than 65 characters.**
Title has been reduced to 60 characters

- **Please always write package names, software names and API (application programming interface) names in single quotes in title and description. e.g: --> 'keras', 'tensorflow'. Please note that package names are case sensitive.**

All packages names in the title, description and documentation has been changed to single quotes. Case has also been reviewed.

## Contribution and Novelty
TSLSTMplus is an enhancement of the existing TSLSTM package, offering advanced features and an improved user interface for LSTM models in R. It addresses several limitations of the original TSLSTM package by providing:

- A more intuitive and user-friendly interface for model training and prediction.
- Additional customization options, including a choice of activation functions and various Keras optimizers.
- Improved scaling functionalities for both input and output data.
- Enhanced validation split capabilities, fixing issues present in the original package.
- Prediction of new data points not used during training.

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
