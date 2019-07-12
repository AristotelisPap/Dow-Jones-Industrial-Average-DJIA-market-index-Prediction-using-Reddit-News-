# Dow-Jones-Industrial-Average-DJIA-market-index-Prediction-using-Reddit-News-

In this project, we predict the Dow Jones Industrial Average (DJIA) market index movement using news and past historical data of the market index. More specifically, we use data coming from the Reddit News as well as data describing the past 'Open', 'High', 'Low' and 'Close' prices of the index and we try to predict whether the price of the index will increase or decrease. Therefore, we formulate the problem as a binary classification problem. 

The news data included the 25 most important topics of each day on Reddit for 8 consecutive years. To preprocess those text data, we used some NLP techniques in order to extract 'Subjectivity' and 'Objectivity' of the news as well as the 'Positive', 'Neutral' and 'Negative' sentiment of the news in the stock price index.

Additionally, before we make the prediction for each day's 'Close' price, we use the 'Open', 'High', 'Low' and 'Close' prices of the index for the past 4 days. In our approach, we also make each algorithm to update its weights every certain number of days in order to keep track of the latest stock prices news, i.e. the algorithm learns how often it should update its weights in order to improve its predictions.

In order to solve the problem, we apply several machine learning algorithms including Logistic Regression with l_2 regularization, Random Forest, AdaBoost and Support Vector Machines with Linear and Gaussian kernels. The performance of the algorithms is evaluated using test set accuracy as well as ROC curves and AUC which are the de facto evaluation metrics for this kind of problems. 

The evaluation of the algorithms show that simpler models like Logistic Regression and Support Vector Machines with Linear kernels behave better than the most sophisticated ones in the particular dataset mainly because of the limited size of the dataset. Finally, the Generalization Bound Inequality is used in order to derive an upper bound for the test accuracy and pick the best out of the models used. Last, a final comparison with already existing techniques from Kaggle is also made showing the superior performance of our approach.


   **Table: Final Results**



|      Model 			| Test Error  	| AUC     	|  
|:-----------------	|:-----------	|:-----------	|
| Logistic Regression with L2 Regularization           	| 37.33 %        | 0.69        | 
| Random Forest          	| 46.66 %        | 0.533        |
| AdaBoost           	| 49.06 %        | 0.563        |
| SVM with Linear Kernel           	| 40.21 %        | 0.682        |
| SVM with Gaussian Kernel           	| 49.59 %        | 0.547        |


