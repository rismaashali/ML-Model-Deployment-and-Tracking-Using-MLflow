# Machine Learning Model Deployment and Tracking Using MLflow

# ML Model Deployment Workflow
1. Use Case Summary
    - Objective Statement
    - Challenges
    - Analytic Method/Technique
    - Business Benefit
    - Expected Outcome
2. Business Understanding
3. Data Understanding
4. Data Preparation
5. Data Profiling
6. Data Cleansing
7. Exploratory Data Analysis
8. Preprocessing Modeling
9. Modeling using Linear Regression
10. Evaluate Model
11. Model Deployment
12. Result
13. Recommendation

# Use Case Summary
- Objective Statement:
  - To get insight how much sales based on tv advertising
  - To get insight how much money is spent on advertising on TV
  - To gain insight into the relationship between sales and TV marketing
  - To predict sales using Linear Regression based on TV advertising
  - To get insight about model deployment using MLflow

- Challenges:
  - There are no other variables as a comparison

- Methodology / Analytic Technique:
  - Descriptive Analysis
  - Graph Analysis
  - Modeling using Linear Regression
  - Model Deployment using MLflow

- Business Benefit:
  - Knowing how much sales from tv advertising
  - Knowing how sales predict results by placing ads on TV
  - Helping business team optimize spent advertising costs

- Expected Outcome:
  - Know how much sales based on TV advertising
  - Know how much money is spent on advertising on TV
  - Know about relationship between sales and TV marketing
  - Know the results of sales prediction using Linear Regression based on TV advertising
  - Know about creating model deployments using MLflow and the results

# Business Understanding
- Tv Marketing is the method of demonstrating features of products and providing their information on television to attract viewers and encourage them to buy the shown products is called trade through television marketing.
- This case has some business question using the data:
   - How much company spent money on TV advertising?
   - How much money is spent on advertising on TV?
   - How about relationship between sales and TV marketing?
   - How about the results of sales prediction based using Linear Regression on TV advertising?
   - How to create a model deployment using MLflow?

# Data Understanding

- Data of TV Marketing
- This data have 2 columns and 200 rows
- Source Code : https://www.kaggle.com/datasets/leiadis/tvmarketing
- Data Dictionary :
  - TV : money spent on advertising via TV
  - Sales : number of sales

# Data Preparation
Code Used:
- Python Version: 3.7.15
- Packages: Pandas, Numpy, Matplotlib, Seaborn, MLFlow, sklearn and Warnings

# Data Profiling
Data profiling is the process of reviewing source data, understanding structure, content and interrelationships, and identifying potential for data projects.

# Data Cleansing
The TV Marketing dataset is clean because the data no longer has missing values and the data types are already appropriate.

# Exploratory Data Analysis
- What about the relationship between sales and TV marketing based on scatterplot?

    ![Screenshot_20221117_114716](https://user-images.githubusercontent.com/113869968/202358667-52ae25b2-3ed8-4439-bf13-aa993a1506d8.png)
    
    From the chart above, it can be seen that there is a **strong relationship** between TV advertising and sales. Based on scatterplot, the relationship between TV advertising and sales is **directly proportional**. As more money is spent on advertising on TV, sales will increase.

- What about the relationship between sales and TV marketing based on correlation values?

    ![Screenshot_20221117_114728](https://user-images.githubusercontent.com/113869968/202358672-8c995eac-ffca-4126-aa17-d1c6d793b213.png)
    
    From the heatmap above, it can be seen that **there is a strong relationship** between TV advertising and sales. This is because the correlation value between sales and tv marketing is **0.78** where it is **more than 0.5**.
    
# Preprocessing Modeling
- **Splitting Train & Test.**
  Before modeling, it is necessary to divide the dataset into two parts, namely the part used for data training and for data testing with a proportion of 1/3.

# Modeling
- **Linear Regression Modelling**, is a type of machine learning algorithm that is used to model the relation between scalar dependent and one or more independent variables. In this case, data training is using to modelling with linear regression and make predictions using the previously trained Linear Regression model.

  ![image](https://user-images.githubusercontent.com/113870005/202447581-f9197648-2c8d-4890-b79b-ba1806d2667c.png)

Based on the scatter plot above, it can be seen that the modeled train data tends to approach the linear line which is the result of the prediction. This means that the data and the predicted results are not much different so it can be said that the data follows a linear regression model.
    
# Evaluate Model
In the last stage, we will evaluate the model using MAE, MAPE, R-Square, and RMSE to see if the model formed is good enough.
- Based on the evaluation of the model using MAE, a fairly small value was obtained and close to 0, which is 2,381. This means that the formed model is good for prediction.
- Based on the evaluation of the model using MAPE, a value of 0.18 or 18% is obtained, where this figure is below 20%. This means that the model formed has good forecasting results.
- Based on the evaluation of the model using R-Square, a value of 0.65 or 65% is obtained. This means that TV advertising has an effect of 65% on sales while the remaining 35% is influenced by other unknown factors.
- Based on the evaluation of the model using the RMSE, a fairly small value was obtained and close to 0, which is 3.06. This means that the model is good enough to make predictions.

# Model Deployment
Based on the model deployment above, the same model evaluation value is generated as the previously obtained evaluation results. If we use visual studio to create the model deployment, it can be displayed mlflow ui below
![image](https://user-images.githubusercontent.com/113869964/202740729-8fc88b8f-564b-4801-93ac-c0ab630dc93e.png)

# Result
- Based on the scatterplot, the relationship between TV advertising and sales is directly proportional. The more advertising on TV, the sales are also increasing.
- Based on the heatmap graph, it can be seen that there is a strong relationship between TV advertising and sales.
- The correlation value on the heatmap obtained is 0.78 where the figure is above 0.5.
- Based on the evaluation of the model using MAE, a fairly small value is obtained, it is 2,381. This means that the model formed is good for predictions.
- Based on the evaluation of the model using MAPE, a value of 0.18 or 18% is obtained, where this figure is below 20%. This means that the model formed has good forecasting results.
- Based on the evaluation of the model using R-Square, a value of 0.65 or 65% is obtained. This means that TV advertising has an effect of 65% on sales while the remaining 35% is influenced by other unknown factors.
- Based on the evaluation of the model using the RMSE, a fairly small value is obtained, namely 3.06. This means that the model is good enough to make predictions.

# Recommendation
- In research other predictor variables can be added so that it is possible to get a better model.
- Companies must optimize the costs spent on advertising through TV because there are some sales are not necessarily high when the money spent on advertising is high.
- We can increase sales by advertising products through social media, news, etc


# MLflow
MLflow is a platform to streamline machine learning development, including tracking experiments, packaging code into reproducible runs, and sharing and deploying models.

MLflow’s current components are:
- MLflow Tracking: An API to log parameters, code, and results in machine learning experiments and compare them using an interactive UI.
- MLflow Projects: A code packaging format for reproducible runs using Conda and Docker, so you can share your ML code with others.
- MLflow Models: A model packaging format and tools that let you easily deploy the same model (from any ML library) to batch and real-time scoring on platforms such as - Docker, Apache Spark, Azure ML and AWS SageMaker.
- MLflow Model Registry: A centralized model store, set of APIs, and UI, to collaboratively manage the full lifecycle of MLflow Models.

Result:
Based on the model deployment, we can track model evaluations based on RMSE, MAE, MAPE, and R-Square in mlflow UI

