# Beer-Volume

Link for the second part (use colab to view the interactive graph) : https://colab.research.google.com/drive/1Fv9DoUXPb8yAAaKCdpyREldhFjEERXKa

**Understanding:**
We have to analyse the Beer Volume data and see how the growth pattern is for the dependent variable i.e Volume_KHL (Volume of the beer in hectolitres). 
For the first step of the problem i.e. building data insights: We have several independent - both numerical and nominal variables in the dataset given. We can perform Exploratory data analysis to understand how the Volume varies based on different situations, for example: if the temperature is high, is the beer consumption also high?; if the GDP of the country of interest (here Argentina) goes down, does it affect the beer consumption; is the beer consumption higher on certain days like during the FIFA season and so on.
For the second step of our problem, i.e model building, we have to analyse the given time series data to build short term and long term forecasts. Taking into consideration the predicted value for the next six months and two years (along with the data insights), we can suggest some sales strategies to be followed by the leaders to increase the volume of beer sold.

**Approach:**
Descriptive analysis, exploratory analysis, diagnosing why certain values are the way they are, predicting for the future, suggesting business strategies based on the forecast and exploratory analysis.
For Step 1: Use Python data libraries like numpy, pandas to order the data, remove the redundant values. Plot the visualisations using matplotlib and seaborn libraries. Gather insights from the graphs on how certain holidays and other macro-economic factors affect the trend. 
For step 2: Use the Prophet model to build a univariate analysis on the volume data. Divide the data into test and validation, look at the values predicted + error obtained (differences between predicted and actual values). Suggest various short term and long term strategies to be followed for higher sales based on predictions.



**Steps Taken:**
1. Importing all the required libraries into the Jupyter notebook (for eg, numpy, pandas, matplotlib, seaborn)
2. Removing the fields where Volume_KHL is null, performing descriptive analysis, for example to see the number of unique values, data types used etc.
3. Plotting the correlation matrix for all the variables. Mainly focus on how independent variables like the country’s GDP, certain holidays, temperatures are correlating/varying with the Beer Volume.
4. Plotting line charts, scatter plots and distplots to see the Volume trend with different variables. 
5. Plotting the Period vs Volume graph to notice the trend of Beer Volume - yearly and monthly.
6. Based on the trend observed (stationary or non-stationary), building an additive auto regression model for time series forecasting. Made use of the FBProphet library to build a univariate analysis for Volume data. Equation used by Prophet: y(t) = g(t) + s(t) + h(t) + ϵ; where: g(t) = overall growth trend; s(t) = yearly seasonality, weekly seasonality; h(t) = holiday effect


**Final Solution:**
It was observed that the sales are higher in the month of December. This is because major holidays like Christmas, new years and Feast_of_the_Immaculate_Conception fall in this month.
It can be seen that the Average and minimum temperatures have a high correlation to the volume, i.e. the consumption is higher when the temperature is higher and vice versa. 
It can also be observed from the graphs that macro-economic factors like the GDP does not affect the trend much, nor does sports holidays like FIFA. 
From the model prediction, we can see that for the next two years there will be a linear increase in the sales. 
