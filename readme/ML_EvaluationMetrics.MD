Machine learning model evaluation metrics:
**********************************************



*********************************************************************************************************************************
https://www.coursera.org/articles/machine-learning-models
https://www.coursera.org/articles/machine-learning-algorithms

How to create a machine learning model ?

            Machine learning models are created by training algorithms with either labeled data, unlabeled data, or a mix of both. Four primary machine learning algorithms exist:

                        Supervised learning:       Supervised learning occurs when an algorithm is trained using “labeled data,” or data that is tagged with a label so that an algorithm can successfully learn from it. Training labels help the eventual machine learning model know how to classify data in the manner that the researcher desires.
                        
                        Unsupervised learning:       Unsupervised algorithms use unlabeled data to train an algorithm. In this process, the algorithm finds patterns in the data itself and creates its own data clusters. Unsupervised learning and pattern recognition are helpful for researchers who are looking to find patterns in data that are currently unknown to them.
                        
                        Semi-supervised learning:   Semi-supervised learning uses a mix of labeled and unlabeled data to train an algorithm. In this process, the algorithm is first trained with a small amount of labeled data before being trained with a much larger amount of unlabeled data. 
                        
                        Reinforcement learning:     Reinforcement learning is a machine learning technique in which positive and negative values are assigned to desired and undesired actions. The goal is to encourage programs to avoid the negative training examples and seek out the positive, learning how to maximize rewards through trial and error. Reinforcement learning can be used to direct unsupervised machine learning.

What are parameters in machine learning?

Types of machine learning models
There are two types of problems that dominate machine learning: classification and prediction.

                        These problems are approached using models derived from algorithms designed for either classification or regression (a method used for predictive modeling). Occasionally, the same algorithm can be used to create either classification or regression models, depending on how it is trained. 
                        
                        Below you will find a list of popular algorithms used to create classification and regression models. 

Classification models:
Logistic regression
Naive Bayes
Decision trees
Random forest
K-nearest neighbor (KNN)
Support vector machine

Regression models:  (A method used for predictive modeling)

                        Linear regression
                        Ridge regression 
                        Decision trees
                        Random forest 
                        K-nearest neighbor (KNN)
                        Neural network regression


1. Linear regression            :a supervised machine learning technique used for predicting and forecasting values that fall within a continuous range, such as sales numbers or housing prices.
2. Logistic regression          :also known as "logit regression," is a supervised learning algorithm primarily used for binary classification tasks.
3. Naive Bayes                  :a set of supervised learning algorithms used to create predictive models for binary or multi-classification tasks.
4. Decision tree                :a supervised learning algorithm used for classification and predictive modeling tasks.
5. Random forest                : an ensemble of decision trees used for classification and predictive modeling.
6. K-nearest neighbor (KNN)     :a supervised learning algorithm commonly used for classification and predictive modeling tasks.
7.  K-means                     :an unsupervised algorithm commonly used for clustering and pattern recognition tasks
8. Support vector machine (SVM) :a supervised learning algorithm commonly used for classification and predictive modeling tasks.
9. Apriori                      :unsupervised learning algorithm used for predictive modeling
10. Gradient boosting           :algorithms employ an ensemble method, which means they create a series of "weak" models that are iteratively improved upon to form a strong predictive model.

Notes:    a decision tree is a common algorithm used for both classification and prediction modeling.


***********************************************************************************************************************************



https://www.analyticsvidhya.com/blog/2019/08/11-important-model-evaluation-error-metrics/

Evaluation metrics are quantitative measures used to assess the performance and effectiveness of a statistical or machine learning model. These metrics provide insights into how well the model is performing and help in comparing different models or algorithms.


Confusion Matrix                            [ For classification ]        
F1 Score                                    [ For classification ]
Root Mean Squared Error (RMSE)
Root Mean Squared Logarithmic Error         [ For Regression Model]   
R-Squared/Adjusted R-Squared
Area Under the ROC Curve (AUC – ROC)        [ For classification ]                  
Gini Coefficient
Gain and Lift Charts
Kolomogorov Smirnov Chart
Log Loss
Concordant – Discordant Ratio
Cross Validation


**********************************************
#)            A confusion matrix is a table that is used to measure the performance of the machine learning classification model(typically for supervised learning, in the case of unsupervised learning is usually called the matching matrix) where output can be two or more classes. Each row of the confusion matrix represents the instances in a predicted class while each column represents the instance in an actual class or vice versa.

                                    --------------------------------------------------------------------------
                                    +                     +   Predcited:  No       +    Predcited:  Yes     +               
                                    +                     +                        +                        +
                                    --------------------------------------------------------------------------
                                    +                     +                        +                       + 
                                    +    Actua:   No      +       TN               +         FP            + 
                                    --------------------------------------------------------------------------
                                    +                     +                        +                        + 
                                    +    Actua:  Yes      +       FN               +         TP             + 
                                    --------------------------------------------------------------------------

                        A confusion matrix is also known as an error matrix.

                        
                         Now let’s understand what are TP, FP, FN, TN.
                        
                        Here we have two classes, Yes and No, then we define,
                        
                        TP-True positive: You predicted Yes class and its actual class is also Yes.
                        TN-True negative: You predicted No class and its actual class is No.
                        FP-False positive: You predicted the Yes class but actually it belongs to the No class. It is also called type 1 error.
                        FN-False Negative: You predicted No class but actually it belongs to the Yes class. It is also called a type II error.
                        
                        So, what are the classification performance metrics that we can calculate from the confusion matrix? Let’s see.            https://vidyasheela.com/post/what-is-confusion-matrix


                        By observing the confusion matrix we can calculate the Accuracy, Recall, Precision, and F1-score(or F measure) of the classification model. Let’s understand them by taking an example of a confusion matrix.


#)            F1-Score or F-measure is an evaluation metric for a classification defined as the harmonic mean of precision and recall. It is a statistical measure of the accuracy of a test or model. Mathematically, it is expressed as follows,
f1 score =  (2 * Recall* precision) /   Recall + Precision
Here, the value of F-measure(F1-score) reaches the best value at 1 and the worst value at 0. F1-score 1 represents the perfect accuracy and recall of the model.


            Now let’s see what Recall and precision actually means,


                        
                        Recall: It tells us what proportion of Data belonging to a certain class say, class A is classified correctly as in class A by our classifier.            
                                     Recall tells us about when it is actually yes, how often does our classifier predict yes. or it can also be defined as, out of all the positive classes, how much our classifier predicted correctly. It is calculated by using the formula below,
                                                                        
                                                                        RECALL = TP  / TP + FN
                        
                        
                        Precision: It tells us what proportion of data that our classifier has classified in a certain class, say class A actually belongs to the same class A.
                                   Precision: It tells, out of all the classes, how much our classifier predicted correctly. It should be high as possible. In other words, Precision tells us about when it predicts a class, how often is it correct. It is calculated by using the formula below,
                                                                        
                                                                        PRECISION= TP  / TP + FP  
                                    To understand more about precision and recall with a mathematical example, you can visit here.


                        Accuracy: The accuracy of classification can be obtained by using the formula below,
                                                ACCURACY = TP + TN / TP + TN + FP + FN


#)           RMSE:            The Root Mean Square Error (RMSE) is a statistical measure that tells us the average distance between the predicted values from a model and the actual values in the dataset1. It is calculated by taking the square root of the sum of the squared differences between the predicted and observed values1.
The formula to calculate RMSE is as follows:

                                                                        RMSE=nΣ(Pi​–Oi​)2​​      

                                                            where:
                                                
                                                Σ is a symbol that means “sum”
                                                Pi​ is the predicted value for the ith observation in the dataset
                                                Oi​ is the observed value for the ith observation in the dataset
                                                n is the sample size1
                                                
                                                The lower the RMSE, the better a given model is able to “fit” a dataset1. However, it’s important to note that RMSE is scale-dependent and thus should not be used to compare datasets of different scales2. It is always non-negative, and a value of 0 would indicate a perfect fit to the data2. RMSE is sensitive to outliers, as larger errors have a disproportionately large effect on it2


#)             RMSLE:            The Root Mean Squared Logarithmic Error (RMSLE) is a measure used to evaluate the performance of a regression model, especially when the predicted and true values are huge numbers1. It is calculated as the square root of the mean of the squared differences between the logarithm of the predicted values and the logarithm of the actual values12.
The formula to calculate RMSLE is as follows:
RMSLE=nΣ(log(Pi​+1)–log(Oi​+1))2​​
where:

                                                Σ is a symbol that means “sum”
                                                Pi​ is the predicted value for the ith observation in the dataset
                                                Oi​ is the observed value for the ith observation in the dataset
                                                n is the sample size12
                                                
                                                The key difference between RMSE and RMSLE is that RMSLE is less sensitive to the effect of outliers1. In the case of RMSE, the presence of outliers can significantly increase the error term. However, in the case of RMSLE, the outliers are drastically scaled down, therefore nullifying their effect1.
                                                Another important property of RMSLE is that it can be broadly seen as a relative error between the predicted and the actual values1. This means that RMSLE only considers the relative error between the predicted and the actual value, and the scale of the error is not significant1. This makes RMSLE particularly useful when you are more interested in the percentual differences rather than the absolute differences3.


#)             R-Squared:                        R-Squared, also known as the coefficient of determination, is a statistical measure used in regression analysis. It determines the proportion of variance in the dependent variable that can be explained by the independent variable123.
The formula for calculating R-squared is:
R2  =  1−(RSS/TSS)​
where:

                                                R2 represents the required R-Squared value
                                                RSS represents the residual sum of squares
                                                TSS represents the total sum of squares1
                                                
                                                The value for R-squared can range from 0 to 14. A higher R-squared value indicates that the regression model explains more of the variability observed in the target variable2. However, a high R-squared can sometimes indicate problems with the regression model, and a low R-squared may sometimes be obtained in the case of well-fit regression models1. Therefore, it’s important to consider other factors when determining the variability of a regression model1.           

#)            Adjusted Q-Square:                The Adjusted R-Squared is a modified version of R-Squared that adjusts for the number of predictors in a regression model12345. It is calculated as:
Adjusted R2            =            1 − [(1−R2)(n−1)​  /  (n−k−1)]
where:

                                                            R2 is the R-Squared of the model
                                                            n is the number of observations
                                                            k is the number of predictor variables1
                                                            
                                                            The key difference between R-Squared and Adjusted R-Squared is that Adjusted R-Squared accounts for the number of predictors in the model12345. The Adjusted R-Squared increases only if the new term improves the model more than would be expected by chance. It decreases when a predictor improves the model by less than expected12345.
                                                            Because of the way it’s calculated, Adjusted R-Squared can be used to compare the fit of regression models with different numbers of predictor variables1. This makes Adjusted R-Squared particularly useful when you want to prevent overfitting by adding too many predictors to a mode


#)          Area Under the ROC:                  The Area Under the Receiver Operating Characteristic Curve (AUC-ROC or AUC) is a performance measurement for classification problems at various thresholds settings1234. The ROC curve is a plot of the True Positive Rate (TPR) against the False Positive Rate (FPR) at various threshold settings1.

                                                The AUC represents the degree or measure of separability. It tells how much the model is capable of distinguishing between classes1. The higher the AUC, the better the model is at predicting 0s as 0s and 1s as 1s1. An excellent model has AUC near to the 1 which means it has a good measure of separability1. A poor model has AUC near to the 0 which means it has a worse measure of separability1. In fact, when AUC is approximately 0, the model is actually reciprocating the classes1.
                                                
                                                AUC is desirable for the following two reasons1:
                                                
                                                AUC is scale-invariant. It measures how well predictions are ranked, rather than their absolute values1.
                                                AUC is classification-threshold-invariant. It measures the quality of the model’s predictions irrespective of what classification threshold is chosen1.
                                                However, both these reasons come with caveats, which may limit the usefulness of AUC in certain use cases1:
                                                
                                                Scale invariance is not always desirable. For example, sometimes we really do need well-calibrated probability outputs, and AUC won’t tell us about that1.
                                                Classification-threshold invariance is not always desirable. In cases where there are wide disparities in the cost of false negatives vs. false positives, it may be critical to minimize one type of classification error1



#)            Gini Coeffiecinet:                        The Gini Coefficient, also known as the Gini index or Gini ratio, is a measure of statistical dispersion intended to represent the income inequality, wealth inequality, or consumption inequality within a nation or a social group1. It was developed by Italian statistician and sociologist Corrado Gini1.

                                                The Gini Coefficient measures the inequality among the values of a frequency distribution, such as levels of income1. A Gini Coefficient of 0 reflects perfect equality, where all income or wealth values are the same, while a Gini Coefficient of 1 (or 100%) reflects maximal inequality among values, a situation where a single individual has all the income while all others have none1.
                                                
                                                The Gini Coefficient is useful because it projects negative values for income and wealth which standard measures of inequality are unable to provide2. However, it does have its limitations. For example, it samples people at random points of their lives, which means that it can’t separate those whose financial futures are reasonably secure from those who do not have prospects, even in a large sample2.
                                                
                                                In an economic context, the Gini Coefficient is important to understand as it provides an estimation of how far a country’s wealth or income distribution deviates from an equal distribution2. For OECD countries in the late 20th century, considering the effect of taxes and transfer payments, the income Gini Coefficient ranged between 0.24 and 0.49, with Slovenia being the lowest and Mexico the highest


#)

**********************************************
chi-squre                             (Used for categorical attributes - classfication problems, higher the chi score value higher the importance of target variable. Higher the P value then its more independent and so less important for target variable )            https://www.youtube.com/watch?v=6N9H9KxdZdk
Pearson Correlation Matrix            (Used for continueous vlues, Correlation Value higher than 0.5 and close to 1.0 target variable then we drop these attributes in certain cases. These attributes are important in finding the target variable and so data leak.)            https://www.youtube.com/watch?v=1fFVt4tQjRE
Covariance and Correlation            https://www.youtube.com/watch?v=2bcmklvrXTQ

Feature Selection, Forward Feature Selection
Finding and droping unwanted attributes/features
Fiding and removing outliers in data

Recursive Feature Elimation
Heatmap
Normalization:            Decimal Scale Normalization, Min Max Normalization, Z score Normalization

Cross validation in ML

Hyperparameters vs parameters:                        A hyperparameter is an entity of a learning algorithm, usually (but not always) having a finite numerical value. That value affects the way the algorithm works. Hyperparameters are not learned by the algorithm itself from data but we set them. They have to be set by the data analyst before running the algorithm.            
For example, the value of ‘K’ in K-NN algorithm, number of hidden neurons in the hidden layer of the neural network, filter or kernel size in the Convolutional neural network, etc.

Parameters are variables that define the model, learned by the learning algorithm. Parameters are directly modified by the learning algorithm based on the training data. The goal of learning is to find such values of parameters that make the model optimal in a certain sense.

            For example, weights ‘w’ and bias ‘b’ in linear regression and neural networks.

Loss functions & cost functions

Epoch vs Batch Size vs Iterations

************************************
Testing:
************************************
Statistical Testing
Hypothesis Testing
T Test
Z Test
Anova
Chi


**********************************************
Classification evaluation metrics…
===================================

Accuracy:	# of correctly classified instances / # of all instances

Precision & Recall are classificationmatrices and mainly depends on TP (True and classified as True), TN (False and classified as False), FP  (False but classified as True) & FN  (True but classified as False)

Precision: % of correctly labelled positive instances out of all positively labelled instances. TP/(TP+FP)

Recall: % of correctly labelled positive instances out of all positively instances. TP/TP+FN

F1 score: combination of precision and recall. Used in combination with other, 2 / (1/precision)+(1/recall)

PR curve:

AUC (area under curve)

Crossentropy:


Regression evaluation metrics:
================================

MAE (mean absolute error)
MSE (Mean squared error):
RMSE (root. Evan squared error)
R2 (coefficient of determination)
Cosine similarity


Libraries:
**************

SciKit
Keras
Tensor flow


Building Machine Learning Model / Training:


Build a Step-by-step Machine Learning Model Using R:                      https://www.analyticsvidhya.com/blog/2022/06/build-a-step-by-step-machine-learning-model-using-r/


***********************************************************************************************************************************
Example Use cases:


https://www.kaggle.com/code/erick5/predicting-house-prices-with-machine-learning


***********************************************************************************************************************************
https://machinelearningmastery.com/statistics_for_machine_learning/

**********************************************************************************************************************************
https://courses.analyticsvidhya.com/courses/applied-machine-learning-beginner-to-professional

20            Machine Learning Lifecycle
21            Problem statement and Hypothesis Generation
22            Importance of Stats and EDA
23            Understanding Data
24            Probability
25            Exploring Continuous Variable
26            Exploring Categorical Variables
27            Missing Values and Outliers
28            Central Limit theorem
29            Bivariate analysis - Introduction
30            Continuous - Continuous Variables
31            Continuous Categorical
32            Categorical Categorical
33            Multivariate Analysis
34            Assignments
35            Build Your First Predictive Model
36            Evaluation Metrics
37            Preprocessing Data
38            Build Your First ML Model: k-NN
39            Selecting the Right Model
40            Linear Models
41            Project: Customer Churn Prediction
42            Dimensionality Reduction (Part I)
43            Decision Tree
44            Feature Engineering
45            Share your Learnings
46            Project: NYC Taxi Trip Duration prediction
47            Working with Text Data
48            Naïve Bayes
49            Multiclass and Multilabel
50            Project: Web Page Classification
51            Basics of Ensemble Techniques
52            Advance Ensemble Techniques
53            Project: Ensemble Model on NYC Taxi Trip Duration Prediction
54            Share your Learnings
55            Hyperparameter Tuning
56            Support Vector Machine
57            Working with Image Data
58            Project: Malaria Detection using Blood Cell Images
59            Advance Dimensionality Reduction
60            Unsupervised Machine Learning Methods
61            Working with Large Datasets: Dask
62            Automated Machine Learning
63            Introduction to Neural Network
64            Forward and Backward Propagation
65            Activation Functions
66            Optimizers
67            Loss Function
68            Project: NN on structured Data
69            Assignment 1 - Big Mart
70            Interpretability of Machine Learning Models
71            Model Deployment
Certificate of Completion

Upon successful completion of the course, you will be provided a block chain enabled certificate by Analytics Vidhya with lifetime validity.

