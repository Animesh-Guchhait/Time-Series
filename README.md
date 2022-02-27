# Time-Series
In this assignment, stock prise data will be predicted using ARMA and GARCH models and their performence will be measured.

Two procedures will be preformed:  $\frac{2}{8}$

At very first, cleaning and processing will be performed on the data and log return column will be generated from stock price.Then we will split the data as train data and test data.Some descriptive ststistics will be performed on the train data to know some statistical features of the data.Then stationarity of log return will be checked on train data. Generally log return data are stationary.In case it is not, we will go for further transformation.

After cleaning, processing and confirming the stationarity of the data, appropriate ARMA model will be fitted on it. Now we will get residual from that model on train data.Then we will perform the Ljung - Box test first on residual, and then on $residual^2$. If the null hypothesis is accepted for residual and is rejected for $residual^2$,we will go for further procedure.

1. Procedure 1:
Uaing above mentioned ARMA model,we will predict future returns and stock prises.Then appropriate GARCH model will be fitted to know future volatility of the returns and stock prises.Performance of the prediction will be measured on the stock prise using the test dataset.


2. Procedure 2:
We have already fitted ARMA model and have got residual from that model on train data. We will fit appropriate ARMA model on $residual^2$ and will predict future $residual^2$.We know that $\epsilon_t=\sigma_t a_t$, where $a_t$ comes from N(0,1). So, Now future $residual_t=sign(a_t)\sqrt(residual_t^2)$. Our new modified predicted retrun $r_t^{modi}=r_t + residual_t$, where $r_t$ is predicted return from ARMA and from $r_t^{modi}$ we will get modified predicted price $y_t^{modi}$ also. So in this way we will get modified forcasts of stock prices.Performance of this procedure will be measured on test dataset.
