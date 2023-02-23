# Accuracy Paradox

Accuracy Paradox for Predictive Analytics states that Predictive Models with a given level of Accuracy may have greater Predictive Power than Models with higher Accuracy. That's why it's not a good idea to use Accuracy as the only metric for evaluating the performance of a Predictive Model.

# CAP Curve

CAP = Cumuliative Accuracy Profile (not ROC = Receiver Operating Characteristic)

It's a curve, which shows the relationship between the True Positive Rate and False Positive Rate for a given Predictive Model. The area under the curve is the Accuracy of the Model. The closer the curve is to the upper left corner (or the greater area under the curve is), the better the Model is.

How to analyze the CAP Curve:
We calculate area between random model and good model (AR), and perfect model and good model (AP). Then we create statistic AR/AP which returns value between 0 and 1. The closer to 1, the better the model is.

Second approach: We look at 50% on the x-axis and read the y-value. 

|y-value | Model evaluation  |
| ------------- | ------------- |
| < 60% | Rubbish  |
| 60% - 70% | Poor  |
| 70% - 80% | Good  | 
| 80% - 90% | Very good  |
| > 90% | Too Good (model might be overfitting)  |

# What model to choose

- If your problem is linear, you should go for Logistic Regression or SVM.
- If your problem is non linear, you should go for K-NN, Naive Bayes, Decision Tree or Random Forest.
- Logistic Regression or Naive Bayes when you want to rank your predictions by their probability. For example if you want to rank your customers from the highest probability that they buy a certain product, to the lowest probability. Eventually that allows you to target your marketing campaigns. And of course for this type of business problem, you should use Logistic Regression if your problem is linear, and Naive Bayes if your problem is non linear.
- SVM when you want to predict to which segment your customers belong to. Segments can be any kind of segments, for example some market segments you identified earlier with clustering.
- Decision Tree when you want to have clear interpretation of your model results,
- Random Forest when you are just looking for high performance with less need for interpretation. 

