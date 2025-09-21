# 📈 Time Series Analysis – ARIMA Modeling in R

## 📌 Description
This project is a **time series analysis** conducted in **R** as part of an academic assignment.  
The main objective is to study and model the series **Seasonally and calendar-adjusted industrial production index – Grain milling (NACE Rev. 2, class 10.61)** from **January 1990 to March 2025** (source: [INSEE](https://www.insee.fr/fr/statistiques/serie/010767639#Graphique)).  

The study follows the classical steps of time series analysis:  
- Data preparation and visualization  
- Stationarity tests and differencing  
- Identification and estimation of an ARIMA model  
- Model validation (Ljung-Box test, residual analysis)  
- Forecasting and construction of confidence regions  

---

## 🛠 Methodology
1. **Stationarity**  
   - The original series shows a trend → first-order differencing applied.  
   - ADF, Phillips-Perron, and KPSS tests confirm stationarity of the differenced series.  

2. **ARIMA Modeling**  
   - ACF/PACF analysis suggests ARMA(p,q) candidates with p ≤ 5, q ≤ 1.  
   - AIC/BIC criteria select **ARIMA(1,1,1)** as the optimal model.  
   - Estimated coefficients:  
     - AR(1) = 0.391  
     - MA(1) = -0.829  
   - Ljung-Box test confirms residuals are mostly uncorrelated.  

3. **Forecasting**  
   - Short-term forecasts generated for (T+1, T+2).  
   - Construction of a **95% joint confidence ellipse** for (XT+1, XT+2).  
   - Visualization of predictions with confidence intervals.  

---

## 📊 Results
- The **ARIMA(1,1,1)** model effectively captures the series dynamics.  
- Residuals behave as white noise.  
- Forecasts are consistent with recent trends and show limited uncertainty.  

📑 For detailed results and plots, see [ST.pdf](./ST.pdf).  
