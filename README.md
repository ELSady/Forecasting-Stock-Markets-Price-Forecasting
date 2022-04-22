## Data Science Project Forecasting : Stock Markets Price with Auto ARIMA and FBProphet Overview
* Analyze the time series of how certain stock market price changes over the years.
* Time series stationary checking using Dickey Fuller Method
* Time series differentiation to make it stationer. Ensuring the Arima model works for the data.
* Time serires Decomposition, separating the trend, seasonal and residual components.
* Preparing time series dataset for forecasting
* Build Forecasting Model and predict the Prices.

### Code and Resources used
**Packages**: pandas, numpy, datetime, matplotlib, seaborn, statsmodel, pmdarima, fbprphet.

### Time Series Visualization
![alt text](https://github.com/ELSady/Forecasting-Stock-Markets-Price-Forecasting/blob/main/index.png)

### Stasionary Checking
![alt text](https://github.com/ELSady/Forecasting-Stock-Markets-Price-Forecasting/blob/main/index1.png)

Looking at at the big difference between rolling mean and its standard deviation, it is very clear that the serires is not stationary. The p value is also greater than 0.05 then, the null hypothesis (time serires stationary) is rejected.

Dickey Fuller Result
> Test Statistics                   0.495121 <br>
> p-value                           0.984724 <br>
> No. of lags used                  4.000000 <br>
> Number of observations used    1757.000000 <br>
> critical value (1%)              -3.434077 <br>
> critical value (5%)              -2.863186 <br>
> critical value (10%)             -2.567646 <br>

### Decomposition 
![alt text](https://github.com/ELSady/Forecasting-Stock-Markets-Price-Forecasting/blob/main/index2.png)

### Preparing Series before forecasting 
Apply log transformation to the series
![alt text](https://github.com/ELSady/Forecasting-Stock-Markets-Price-Forecasting/blob/main/index7.png)

### AUTO ARIMA Model Building
![alt text](https://github.com/ELSady/Forecasting-Stock-Markets-Price-Forecasting/blob/main/index3.png)

### Arima Forecast
![alt text](https://github.com/ELSady/Forecasting-Stock-Markets-Price-Forecasting/blob/main/index4.png)

### FBProphet Forecast and Components
Forecasting <br>
![alt text](https://github.com/ELSady/Forecasting-Stock-Markets-Price-Forecasting/blob/main/index5.png) <br>

Components <br>
![alt text](https://github.com/ELSady/Forecasting-Stock-Markets-Price-Forecasting/blob/main/index6.png)
