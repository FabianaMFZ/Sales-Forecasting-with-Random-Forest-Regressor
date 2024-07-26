### Challenge_random-forest-regressor

For this challenge, we conducted Exploratory Data Analysis to gain insights into the historical data of a specific store. The goal was to identify key features and select the most suitable Machine Learning model to forecast sales for the upcoming semester.

During the EDA process and analysis of graphs, we observed significant statistical variances among different groups and identified features that exhibited stronger correlations with our target variable - sales.

Initially, we conducted a correlation matrix between sales and independent variables such as 'day_of_week', 'nb_customers_on_day', 'open', 'promotion', 'state_holiday', 'school_holiday', 'day', 'month', and 'year'. Notably, the number of customers on a given day ('nb_customers_on_day') showed the highest correlation with sales.

We first attempted a linear regression model to predict sales, but the root mean square error (RMSE) was higher than anticipated. Subsequently, we experimented with a decision tree model, which showed a slight improvement.
To enhance our model's understanding of the data, we decided to segment the data into two groups - closed days and open days - as sales were consistently zero on closed days. However, when we applied another decision tree model, the RMSE increased and the R2 value decreased, as expected due to the absence of accurate predictions for zero sales.

In order to refine our model, we engineered specific features, including columns like 'Store ranking by sum of sales', 'Customer count rank by store', and 'Average customers per day of the week for each store'. Our final feature selection for training, based on higher correlations and lower p-values, included 'nb_customers_on_day', 'avg_customers_per_day_of_week', 'promotion', 'day_of_week', 'store_customer_rank', 'store_sales_rank', and 'sales'.

With our Decision Tree model, we achieved an R2 value of 0.96 and a root mean square error of 656.9465097038384. Following a grid search incorporating KFold cross-validation, we determined the optimal parameters for a Random Forest model, resulting in an improved R2 value of 0.97 and a reduced root mean square error of 531.9750265833966. The strategic inclusion of new columns representing relationships between key features significantly contributed to the success of our model.

Furthermore, we compared our predicted sales with the actual data and found minimal margin of error.
