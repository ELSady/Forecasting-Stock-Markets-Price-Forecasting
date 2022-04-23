## Data Science Project Forecasting : Stock Markets Price with Auto ARIMA and FBProphet Overview
* Analyze the time series of how certain stock market price changes over the years.
* Time series stationary checking using Dickey Fuller Method
* Time series differentiation to make it stationer. Ensuring the Arima model works for the data.
* Time serires Decomposition, separating the trend, seasonal and residual components.
* Preparing time series dataset for forecasting
* Build Forecasting Model and predict the Prices.

### Code and Resources used
* **Packages**: pandas, numpy, datetime, matplotlib, seaborn, statsmodel, pmdarima, fbprphet.

### Time Series Visualization
![alt text](https://github.com/ELSady/Forecasting-Stock-Markets-Price-Forecasting/blob/main/index.png)

* As per the above plot, the prices of Nvidia stock market started rising at around 2016 - 2017. Mo surprise because at this time period cryptomining is becoming a thing.

### Stasionary Checking
![alt text](https://github.com/ELSady/Forecasting-Stock-Markets-Price-Forecasting/blob/main/index1.png)

* Looking at at the big difference between rolling mean and its standard deviation, it is very clear that the serires is not stationary. The p value is also greater than 0.05 then, the null hypothesis (time serires stationary) is rejected.

* Dickey Fuller Result
> Test Statistics                   0.495121 <br>
> p-value                           0.984724 <br>
> No. of lags used                  4.000000 <br>
> Number of observations used    1757.000000 <br>
> critical value (1%)              -3.434077 <br>
> critical value (5%)              -2.863186 <br>
> critical value (10%)             -2.567646 <br>

### Decomposition 
![alt text](https://github.com/ELSady/Forecasting-Stock-Markets-Price-Forecasting/blob/main/index2.png)

* The trend and seasonily decmoposition. The existence of those 2 componnets indicated that the series is not stasionary

### Preparing Series before forecasting 
* Apply log transformation to the series. It is done to remove the trend components and flatten out the its standard deviation.

![alt text](https://github.com/ELSady/Forecasting-Stock-Markets-Price-Forecasting/blob/main/index7.png)

### AUTO ARIMA Model Building
* Automated ARIMA model for the series. AUTO ARIMA simplifies the user to define which parameters, the likes of AR (p), MA (q) and differentitation (d) suit the series best.

![alt text](https://github.com/ELSady/Forecasting-Stock-Markets-Price-Forecasting/blob/main/index3.png)

* ARIMA model plot interpretation:
* **Standardized residual**: The residual errors  fluctuate around a mean of zero and have a uniform variance.
* **Histogram**: The density plot suggest normal distribution with mean.
* **Theoretical Quantiles**: Mostly the dots fall perfectly in line with the red line. Any significant deviations would imply the distribution is skewed.
* **Correlogram**: The Correlogram, (or ACF plot) shows the residual errors are not autocorrelated. The ACF plot would imply that there is some pattern in the residual errors which are not explained in the model.

### Arima Forecast

![alt text](https://github.com/ELSady/Forecasting-Stock-Markets-Price-Forecasting/blob/main/index4.png)

### FBProphet Forecast and Components
* Forecasting with FBProphet <br>

![alt text](https://github.com/ELSady/Forecasting-Stock-Markets-Price-Forecasting/blob/main/index5.png) <br>

* Components <br>

![alt text](https://github.com/ELSady/Forecasting-Stock-Markets-Price-Forecasting/blob/main/index6.png)

FBPropet can return each of the series componnets such as trend, seasonality (weekly and yearly) after forecasting. Here the insight we can get from this Nvidia stock market price over the years :
* Nvidia stock market started increasing at the start of 2016. Interestingly, this is where the year they release the Pascal architechture GPU, the most popular GPU variatns which is still holds up till this moment in time. Another thing worth mentioning also because the rise of crypto currencies value and cryptomining that year directly affects the pricing of said GPU.
* On weekly basis, on average friday, saturday and sunday prices are at the highest, meanwhile monday is the lowest during the week.
* On monthly basis, on average 
* 4
*
