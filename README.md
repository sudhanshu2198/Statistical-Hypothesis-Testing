

# Statistical Hypothesis Testing in ML

Hypothesis Testing is a type of statistical analysis in which you put your assumptions about a population parameter to the test. It is used to estimate the relationship between 2 statistical variables and to present evidence of the plausibility of the null hypothesis.

- The null hypothesis is typically an equality hypothesis between population parameters; for example, a null hypothesis may claim that the population means return equals zero. 
- The alternate hypothesis is essentially the inverse of the null hypothesis (e.g., the population means the return is not equal to zero). 
They are mutually exclusive, and only one can be correct.

**The main goal of this project is to perform extensive statistical hypothesis testing on Credit Card Defaulter Prediction Dataset.**

## 🔗 Links

- [Dataset](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset)
- [Kaggle Notebook](https://www.kaggle.com/code/sudhanshu2198/statistical-hypothesis-testing-in-ml)

## 🛠 Frameworks
Numpy, Pandas, Matplotlib, Seaborn, Scikit-learn, Scipy

## Statistical Hypothesis test

### Normality Test
- An important decision point when working with a sample of data is whether to use parametric or nonparametric statistical methods. Parametric statistical methods assume that the data has a known and specific distribution, often a Gaussian distribution. If a data sample is not Gaussian, then the assumptions of parametric statistical tests are violated and nonparametric statistical methods must be used.
- There are a range of techniques that you can use to check if your data sample deviates from a Gaussian distribution, called normality tests.
![](https://github.com/sudhanshu2198/Statistical-Hypothesis-Testing/blob/main/images/1.PNG)
![](https://github.com/sudhanshu2198/Statistical-Hypothesis-Testing/blob/main/images/2.PNG)
### Non Parametric Variables
We have six month data for Bill amount(BILL_AMT), payment amount(PAY_AMT) and payment repayment status(PAY), we want to know if the variables are redundant (that they provide same information there is no value addition) and irrelavent (they do not affect the target variable)

- We will also check if variables have the same distribution using Friedman test
- The Friedman test is the nonparametric version of the ANOVA.
  - Fail to Reject H0: Paired sample distributions are equal.
  - Reject H0: Paired sample distributions are not equal.

### Chi Independency Test
The Chi-Squared test is a statistical hypothesis test that assumes (the null hypothesis) that the observed frequencies for a categorical variable match the expected frequencies for the categorical variable.

- Ho: Variables are independent
- H1: Variables are dependent

  ![](https://github.com/sudhanshu2198/Statistical-Hypothesis-Testing/blob/main/images/5.PNG)
  ![](https://github.com/sudhanshu2198/Statistical-Hypothesis-Testing/blob/main/images/6.PNG)
  ![](https://github.com/sudhanshu2198/Statistical-Hypothesis-Testing/blob/main/images/7.PNG)

### ANOVA
ANOVA Test could be used to determine whether the different model performances scores have different or same distribution. ANOVA is a statistical test that assumes that the mean across 2 or more groups are equal. If the evidence suggests that this is not the case, the null hypothesis is rejected and at least one data sample has a different distribution.

![](https://github.com/sudhanshu2198/Statistical-Hypothesis-Testing/blob/main/images/8.PNG)
![](https://github.com/sudhanshu2198/Statistical-Hypothesis-Testing/blob/main/images/9.PNG)
![](https://github.com/sudhanshu2198/Statistical-Hypothesis-Testing/blob/main/images/10.PNG)

- LightGBM performs best among other models.
- KNNClassifier performs poorly and is highly underconfident for predicting positive class.
- LightGBM, XGB, Random Forest, Logistic Regression classifiers have learned the underlying structure but are underconfident with high probabilities, therefore there performance can be increased by using probability calibration.









