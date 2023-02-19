# R-Squared

Property for estimating fit of regression model.

$R^2 = 1 - \frac{SS_{res}}{SS_{tot}} = 1 - \frac{\sum{(y_i - \widehat{y_i})^2}}{\sum{(y_i - y_{avg})^2}}$

Rule of thumb (it highly depends on the context):

| R value | Conclusion |
| ------- | ---------- |
|  1.0    |  Perfect fit (suspicious)           |
|  ~0.9   |  Very good                          |
|  <0.7   |  Not great                          |
|  <0.4   |  Terrible                           |
|  <0     |  Model makes no sense for this data |

# Adjusted R-Squared

Problem: we add new independent variable to model.

Observation: $SS_{tot}$ doesn't change and $SS_{res}$ will decrease or stay the same (because of Ordinary Least Squares: $SS_{res}$ -> min).

Solution:

$Adj R^2 = 1 - (1-R^2) \times \frac{n-1}{n-k-1}$, where $k$ is the number of independent variables and $n$ is the sample size.

Adjusted R-Squared *shows whether adding additional predictors improve a regression model or not* (accounts for predictors that are not significant in a regression model).