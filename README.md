# Time-Series
## TSLA stock prise prediction using ARMA and GARCH

In this assignment, stock prise data will be predicted using ARMA and GARCH models and their performence will be measured.

Two procedures will be preformed:

At very first, cleaning and processing will be performed on the data and log return column will be generated from stock price.Then we will split the data as train data and test data.Some descriptive ststistics will be performed on the train data to know some statistical features of the data.Then stationarity of log return will be checked on train data. Generally log return data are stationary.In case it is not, we will go for further transformation.

After cleaning, processing and confirming the stationarity of the data, appropriate ARMA model will be fitted on it. Now we will get residual from that model on train data.Then we will perform the Ljung - Box test first on residual, and then on ![formula]($residual^2$). If the null hypothesis is accepted for residual and is rejected for ![formula]($residual^2$),we will go for further procedure.

