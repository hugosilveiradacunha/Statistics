# Statistics
Experiments Analysis


 [ANOVA and Non Parametric Counterparts](https://github.com/hugosilveiradacunha/Statistics/blob/master/ANOVANonparametricCounterpart.ipynb)

This is a practical approach to a set of statistical techniques commonly used in One-way ANOVA process and nonparametric counterparts.

The main objective was: to apply, interpret and compare the results of a limited set of parametric and non-parametric tests appropriate to solve a specific marketing problem.


# STATISTICS - ANOVA & NONPARAMETRIC COUNTERPART
## 1. INTRODUCTION

## 2. METHODOLOGY

I have included output from two statistical software packages, R and SAS, and try to complement both data analysis and analysis of experiments with some code, mix some text with the code, and publish this work as a notebook.

Firstly, I will do an exploratory data analysis, describing the main statistics and plotting useful information to better understand the data under analysis.

The objective is to test the equality of the six populations’ means, i.e., test if for the different age groups the mean of purchases for the given period is the same in all its levels.

where $i,j = 1, 2, ..., 6 $, are the number of levels.

If $H_0$ is true, the mean values are all equal, thus it was obtained a set of 6 samples withdrawn from the same population.
2.1. ONE-WAY ANOVA WITH FIXED EFFECTS

To test $H_0$, the analysis of the variances of different populations (age groups), popularly known as ANOVA, should be applied.

    Experimental units: customers.

    Factors: age group, with 6 levels: "18-25", "26-35", "36-45", "46-55", "56-65" and "66-90".

    Groups: 6 age groups (treatments)

STATISTICAL MODEL

To fit our model, we will use the sample mean:

corresponding to the age-group.

However, to perform this analysis, we must validate the respective assumptions:

    Independence condition of the observations;

    Normal populations;

    Homoscedasticity.

2.1.1. Independence condition of the observations

To conduct this study, an independent random sample of customers was obtained from each of the six age groups and each customer can only belong to one of each age group.
2.1.2. Normal populations

We will test the normality condition using the following test statistics:

    Lilliefors’ test

    Shapiro-Wilk test

to test:

Considering that we have a satisfactory transformation that gives us a good fit to normality for $\lambda = 0$: $Y = ln(Sales_i)$, we will carry on both variables assuming, however, that they will follow different paths along the one-way ANOVA process and nonparametric counterparts. This approach will give us the possibility to go through multiple steps of the proposed methodology, the opportunity to apply multiple tests and, on the other hand, will also give us alternative results to be compared.
2.1.3. Populations with the same variance

If the normality condition is verified, the hypothesis of homoscedasticity will be tested:

We will test the homoscedasticity condition using the following test statistics:

    Bartlett’s test.

    Levene’s test

2.1.4. ANOVA

To test $H_0$, the analysis of the variances of different age groups, the model errors are assumed to be normally and independently distributed random variables with mean zero and variance $\sigma ^2$. The variance $\sigma^2$ is assumed to be constant for all Age Groups. In this experiment, we will use the transformed variable $Y = ln(X)$.
2.1.5. MULTIPLE COMPARISON TESTS

If we assume normality and homoscedasticity but we reject the null hypothesis, $H_0 : \mu_1 = ...= \mu_6$, it only allows to conclude the non-equality between the mean values of the 6 groups. In this case, we will perform multiple comparisons tests to validate if there is evidence of differences between the mean behavior of the age groups regarding the amount spent, using the following test statistics:

    Tukey's HSD test;

    Hochberg (GF2);

    Scheffé’stest;

to test:
2.3. NONPARAMETRIC COUNTERPART OF ANALYSIS OF VARIANCE

For the original data where the normality assumption is violated, we will use an alternative method to the analysis of variance that does not depend on normality assumptions, the nonparametric tests are applicable regardless of the distribution’s form (distribution-free). However, in general, the parametric tests are more powerful than the nonparametric ones, that´s the reason we must validate the ANOVA assumptions before applying these tests.
2.3.1. Non Normal Populations

As we can't assume normality using original data, we will use the following test statistic:

    Kruskal-Wallis test

to test:
2.3.2. Nonparametric Multiple Comparison Tests

If either normality or homocedasticity condition can't be assumed and we have rejected any of the hypothesis:

    $H_0$ : The 6 samples come from the same population, or from identical populations

    $H_0$ : The 6 normal populations have the same mean

then we will use Nonparametric Multiple Comparison Tests:

    Hodges-Lehmann test for independent samples;

    Dwass-Steel-Critchlow-Flignertest;

    Nemenyitest (or Nemenyi-Damico-Wolfe-Dunn test);

    Conover-Inman test;

    Wilcoxon-Mann-Whitney test (i.e., Mann-Whitney U test) with the Bonferroni correction.

to test if two populations have the same median.
