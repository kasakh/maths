
# Assumptions in Linear Regression

*This is post explaining what are the popular assumptions involved in Linear Regression and their importance*

Most people usually think that 'output' of Linear Regression is only valid when the Linear, Independent, Normal and Constant assumptions are satisfied on the error terms. This is a post explaining what if those assumptions are violated.  

Let me start off by asking one basic question. 

Let us assume that we have our entire population of univariate datapoints $(X_1, Y)$ with us. If one were to minimize square error on this data and get the parameters $b_0,b_1$ where $Y = b_0 + b_1*X_1$ (1), but the error terms do not follow the above mentioned assumptions, what next?

Actually, you can safely use this model for predicting relationship between $X_1 & Y$. There is no need to do any F-test or T-test. In fact, only to perform the F-test or t-test, we require the above LINC assumptions. The whole point of testing comes when we are trying to estimate the relationship $b_1$ using the sample data available. 

When we use the sample data and perform OLS, we get an estimate of $b_1$ which is usually denoted as $\beta_1$. The first assumption in LINC, which is Linear, states that $E(\epsilon)=0$, which means that $\beta_1$ is an unbiased estimator of $b_1$. Why?

$Y = \beta_0 +\beta_1 * X_1 +\epsilon$ is our regression equation we get from the sample. Now if $E(\epsilon)=0$, this means that $\hat Y = b_0 + b_1*X_1$. 


This is exactly what is represented by equation (1). What this means that for a given value of $X_1$, there could be multiple values of $Y$ and our equation predicts that mean of these $Y$'s which is $\hat Y$. 

Having said that, the concept of $r^2$ does not depend on these LINC assumptions. So, we can still say what proportion of variation in the dependent variable, within in the sample data, is being explained our regression equation. 
