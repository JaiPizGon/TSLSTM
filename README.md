# TSLSTMplus

## Overview
TSLSTMplus is an enhanced R package for time series forecasting using Long Short-Term Memory (LSTM) models. Building upon the foundation of the TSLSTM package, TSLSTMplus introduces improved user interface (UI) elements and additional functionalities to streamline the process of modeling and forecasting with LSTM networks in R.

[![CRAN status](https://www.r-pkg.org/badges/version/TSLSTMplus)](https://CRAN.R-project.org/package=TSLSTMplus)
[![CRAN_Download_Badge](https://cranlogs.r-pkg.org/badges/grand-total/TSLSTMplus)](https://cranlogs.r-pkg.org/badges/grand-total/TSLSTMplus)

## Installation
You can install the last stable version of TSLSTMplus from CRAN with:
```R
install.packages("TSLSTMplus")
```

You can install the development version of TSLSTMplus from GitHub with:

```R
# install.packages("devtools")
devtools::install_github("JaiPizGon/TSLSTMplus")
```
## Usage
Here is a basic example of how to use TSLSTMplus:

```R
library(TSLSTMplus)
y<-rnorm(100,mean=100,sd=50)
x1<-rnorm(150,mean=50,sd=50)
x2<-rnorm(150, mean=50, sd=25)
x<-cbind(x1,x2)
x.tr <- x[1:100,]
x.ts <- x[101:150,]
TSLSTM<-ts.lstm(ts=y,
                xreg = x.tr,
                tsLag=2,
                xregLag = 0,
                LSTMUnits=5,
                ScaleInput = 'scale',
                ScaleOutput = 'scale',
                Epochs=2)
current_values <- predict(TSLSTM, xreg = x.tr, ts = y)
future_values <- predict(TSLSTM, horizon=50, xreg = x, ts = y, xreg.new = x.ts)
```

## Credits
This package is inspired by and builds upon the concepts and implementations found in the [TSLSTM](https://cran.r-project.org/web/packages/TSLSTM/index.html) package. We express our gratitude to the authors of TSLSTM for their groundbreaking work in the field of LSTM-based time series analysis.

However, we thought that the user interface of the previously cited package had some flaws, such as a lack of capabilities to predict new samples from the trained LSTM model. Therefore, our package offer the following features:

## Features
TSLSTMplus offers a range of advanced features to facilitate robust and flexible time series modeling:

- **Flexible Model Architecture**: Train regression LSTM models with a customizable number of LSTM and Dense layers, starting with LSTM layers followed by Dense layers, and ending with a final one-neuron Dense layer for output.
- **Diverse Optimizers**: Support for a variety of Keras optimizers.
- **Early Stopping**: Utilize EarlyStopping during training to prevent overfitting as described in the [Keras R package](https://tensorflow.rstudio.com/guides/keras/writing_your_own_callbacks).
- **Input and Output Scaling**: Option to scale both inputs and outputs using standard and min-max scalers.
- **Customizable Activation Functions**: Choose different activation functions for LSTM and Dense layers to tailor the model to specific data characteristics.
- **Validated Validation Split**: Improved validation split functionality, addressing bugs found in the original TSLSTM package.
- **Prediction of New Data Points**: Ability to predict new data points, extending the model's applicability beyond the training dataset.


## Citation
If you use TSLSTMplus in your research or work, please consider citing the original work behind TSLSTM:

Paul, R.K. and Garai, S. (2021). "Performance comparison of wavelets-based machine learning technique for forecasting agricultural commodity prices," Soft Computing, 25(20), 12857-12873.

## License

This package is released in the public domain under the General Public License [GPL](https://www.gnu.org/licenses/gpl-3.0.en.html). 

## Association
Package created in the Institute for Research in Technology (IIT), [link to homepage](https://www.iit.comillas.edu/index.php.en) 
