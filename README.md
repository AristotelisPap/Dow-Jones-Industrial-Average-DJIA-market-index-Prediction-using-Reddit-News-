# Dow-Jones-Industrial-Average-DJIA-market-index-Prediction-using-Reddit-News-

In this project, we predict the Dow Jones Industrial Average (DJIA) market index movement using news and past historical data of the market index. More specifically, we use data coming from the Reddit News as well as data describing the past open, high, low and close prices of the index and we try to predict whether the price of the index will increase or decrease. Therefore, we formulate the problem as a binary classification problem. Since the dataset has the form of time-series, we divide it into a training, a validation and a test set and we use the validation set for hyperparameter tuning. Note that since the dataset has some missing values, we initially fill these values with the mean of each feature. In our approach, we make each algorithm to update its weights every certain number of days in order to keep track of the latest stock prices news. How often each algorithm should update its weights is decided through the validation set. In order to solve the problem, we apply several machine learning algorithms including Logistic Regression with l_2 regularization, Random Forest, AdaBoost and Support Vector Machines with Linear and Gaussian kernels. The performance of the algorithms is evaluated using test set accuracy as well as ROC curves and AUC which are the de facto evaluation metrics for this kind of problems. The evaluation of the algorithms show that simpler models like Logistic Regression and Support Vector Machines with Linear kernels behave better than the most sophisticated ones in the particular dataset mainly because of the limited size of the dataset.  Finally, the Generalization Bound Inequality is used in order to pick the best out of the models used and a final comparison with already existing techniques is also made.


</tr>
    <td>
    Logistic Regression <br />
    with L2 regularization
    </td>
    <td>
    37.33%
    </td>
    <td>
    0.69
    </td>
<tr>
    <td>
    Random Forest
    </td>
    <td>
    46.66%
    </td>
    <td>
    0.533
    </td>
</tr>
    <td>
    AdaBoost
    </td>
    <td>
    49.06%
    </td>
    <td>
    0.563
    </td>
<tr>
    <td>
    SVM with <br />
    Linear kernel
    </td>
    <td>
    40.21%
    </td>
    <td>
    0.682
    </td>
</tr>
    <td>
    SVM with <br />
    Gaussian kernel
    </td>
    <td>
    49.59%
    </td>
    <td>
    0.547
    </td>
</tr>
