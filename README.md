Agenda:
Step 1 - Preparation of the data and definitions
Step 2 - GLM Analysis: frequency
Step 3 - GLM Analysis: Costs
Step 4 - Pure premium: adjusting factor - global balance
Step 5 - Atypical treatment

1 - Preparation of the data and definitions

In this chapter, we will import, analyse and prepare the data in order to be able to go to the next chapter, where we will perform GLM analysis.
Intermediate Agenda:
1.1 Import Data
1.2 Descriptive Analysis
1.3 Data Preparation
1.4 Error Functions
1.5 Split training/test sets
1.6 Split between attritional and atypical sets

2 - GLM Analysis: frequency

Here is a non-exhaustive list of packages that can be used to implement GLM:
fastglm : package to fit GLM efficiently using ‘RcppEigen’ (improved speed)
glmnet : LASSO and Elastic-net regularized GLM
Bigglm : Creates a GLM object that uses only p^2 memory for p variables (Large database)
bestglm : Allows the use of CV, and provides new information criteria such BICq, AIC, BIC and EBIC for selecting the best model
glm.deploy : Write a glm model into C or Java
Now, we will model the claim's frequency using GLMs.

3 - GLM Analysis: costs

In this part we will perform a Gamma regression on costs.
We will use the same data as for the frequency analysis. We start by eliminating the lines where the claim amount is equal to zero.

4 - Pure premium: adjusting factor - global balance

We will now use the results obtained in Chapter 2 and Chapter 3 to compute the pure premium for each policyholder.
First we will again use a dataset without atypical claims.

5 - Atypical treatment

In this part, we will deal with the atypical Claims, which were removed in the previous chapters.
We first start by building our updated database, with a new binary column to determine whether or not the claim is Atypical.
