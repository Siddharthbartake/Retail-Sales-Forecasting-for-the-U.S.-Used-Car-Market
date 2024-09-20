# Retail-Sales-Forecasting-for-the-U.S.-Used-Car-Market
This research forecasts U.S. used car retail sales from January 2018 to December 2019 using time-series data from 1992 to 2017. It applies four forecasting methods: Exponential Smoothing, Multiplicative and Additive Decomposition Models, and ARIMA. Models are evaluated using MAPE to determine the most accurate prediction technique.

* **Overview**:
This research focuses on forecasting retail sales of used cars in the United States utilizing time-series data collected from used car dealerships. The dataset comprises monthly sales data, measured in millions of dollars, covering January 1992 to December 2017. The goal is to utilize multiple forecasting methodologies to predict sales for the period spanning January 2018 to December 2019. The selected forecasting techniques, within our curriculum, are as follows:
a. Exponential Smoothing
b. Decomposition Method – Multiplicative Model
c. Decomposition Method – Additive Model
d. ARIMA – Auto-Regressive Integrated Moving Average
The evaluation and comparison of these forecasting models will rely on the Mean Average Percentage Error (MAPE) to ascertain the superior predictive accuracy among the models. This study aims to provide important insights into the optimal forecasting methodology for retail sales of pre-owned cars in the United States. Trying to present a thorough analysis of selected methods and their individual performances, contributes valuable findings to this research.

A.) **Exponential Smoothing**
Utilizing the exponential smoothing forecasting technique, we tested 12 distinct models involving four trends: No Trend, Linear, Damped, and Exponential, and three seasonal levels:
No Seasonality, Additive, and Multiplicative. Through out-of-sample evaluation, we computed the Mean Average Percentage Error (MAPE) for these models. Among them, the model having Exponential Trend and Multiplicative Seasonality exhibited the lowest MAPE, recorded at 2.77.

![image](https://github.com/user-attachments/assets/af560eef-b918-4f46-a6d5-87e01f0f097f)

![image](https://github.com/user-attachments/assets/6aea4322-46de-48ea-9e36-ab782479ff66)
![image](https://github.com/user-attachments/assets/8ecbbe18-8e82-451a-b677-3a18967d02db)
We therefore calculated the out-of-sample accuracy using the actual data, and the MAPE was to be 3.053%.
The conclusion of Exponential Smoothing method is that the best model is Exponential Trend with Multiplicative Seasonality.

B.) Decomposition Model – Multiplicative
In the process of refining forecast accuracy, a multiplicative decomposition model was applied. Initially, 12-month Moving Averages were computed to smooth short-term fluctuations in the data. Subsequently, a centered moving average was calculated. The graphical representation displays the original sales data (depicted by the blue line) juxtaposed with deseasonalized data denoted as Sales_CMA (shown in pink).
The long-term trend was determined using the formula Sales_CMAT = 0.3666 + 19.988757t, where 't' stands for the time variable. Sales_CMAT, denoted by a dashed line in the plot, is how this trend is visually depicted.
By carefully breaking down the sales data, this technique seeks to identify and isolate the underlying trends and seasonality, which will help create a more accurate and perceptive forecasting framework.

![image](https://github.com/user-attachments/assets/6eba82c6-1308-4ad9-9ab2-b5c92659df86)

![image](https://github.com/user-attachments/assets/1f74ed7f-bff7-4632-9773-a50353f5d8fd)

![image](https://github.com/user-attachments/assets/6fe1c479-c58b-49b4-a646-bdc458e4f430)

Each of the components from the previous phases was multiplied to create forecasts for the 2018–2019 by emulating the deconstructed time series. 2.979% is the MAPE of the predicted value compared to the anticipated value.
The below are the MAPE and RMSE for the Multiplicative Decomposition:
![image](https://github.com/user-attachments/assets/bce024fd-46df-41a5-bc17-054a2a69e04e)


C.) Decomposition Method – Additive
The time series was divided into the corresponding components SI, Sales_CMAT, and Sales_CF using additive decomposition, which was done in a manner similar to the multiplicative decomposition model.
The Unadjusted SI for the additive method of breakdown is shown below. Keep in mind that these numbers don't equal 0. They don't cancel one another. We therefore have to change the Values.
![image](https://github.com/user-attachments/assets/38bf1648-7965-4a7b-bc2d-e32bc0abfae2)

The corrected SI values are listed below. They all add up to 0.
![image](https://github.com/user-attachments/assets/e3ad5cd6-a656-4283-bec6-2dee29254e0e)
![image](https://github.com/user-attachments/assets/d4aa251b-f266-4a5c-a697-9a96722dc8df)

D.) Arima
After analyzing the time-series data, the best model for predicting was automatically determined to be ARIMA (0, 1, 1)*(0, 1, 1)*. The outcomes of the forecast are shown below. Two more candidate models were also taken into consideration: ARIMA (0,1,1) (1,1,0) and ARIMA (1,1,0)(1,1,0). The most accurate model for forecasting is the automatically chosen ARIMA model, which has an accuracy of 3.126%, higher than the other two models combined.
![image](https://github.com/user-attachments/assets/bb89f2fa-3413-4757-9056-738abce27d52)
![image](https://github.com/user-attachments/assets/adaedba8-ed7e-4832-a2ac-b2801f69ee20)

* **Conclusion**:
We can see that Multiplicative Decomposition Model performs better than the other four forecasting models after a thorough analysis and performance evaluation was carried out. The out-of-sample forecast has an exceptionally low Mean Absolute Percentage Error (MAPE) of 2.98, indicating its superior accuracy when compared to the MAPEs of 3.053, 4.099, and 3.13 obtained from the Exponential Smoothing (Exponential Trend with Multiplicative Seasonality), Additive Decomposition Model, and ARIMA (Box-Jenkins) Model. The outcomes demonstrate that, among the models under consideration, the Multiplicative Decomposition Model offers the optimum balance between accuracy and efficiency, making it the most dependable option for forecasting.
![image](https://github.com/user-attachments/assets/5b89de9a-4072-4465-a78f-6b0277fb1c7f)

