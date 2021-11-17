<!-- Add banner here -->
![rsz_undraw_yacht_re_kkai](https://user-images.githubusercontent.com/83410546/142136092-8204a08b-96f7-47d6-b394-a0c8aa8f03ec.png)

# Handling-Missing-Data-in-Machine-Learning

<!-- Add buttons here -->
![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/ridhed/Weather-Dataset-Analysis?include_prereleases)
![GitHub last commit](https://img.shields.io/github/last-commit/ridhed/Weather-Dataset-Analysis)
![GitHub issues](https://img.shields.io/github/issues-raw/ridhed/Weather-Dataset-Analysis)
![GitHub pull requests](https://img.shields.io/github/issues-pr/ridhed/Weather-Dataset-Analysis)
![GitHub](https://img.shields.io/github/license/ridhed/Weather-Dataset-Analysis)

<!-- Described the project in brief -->
Handling Missing Data in Titanic Problem using MCAR, MNAR, MAR.


# Table of contents

- [Project Title](#project-title)
- [Objective](#objective)
- [Types of missing data](#types-of-missing-data)
- [Imputation Methods](#imputation-methods)

# Objective 
* There are a variety of reasons that may lead to missing data, such as data corruption, lack of data availability during certain time periods, or bias in the data collection process (e.g. certain categories of respondents in a survey leave an answer blank).
The important distinction to make here is whether or not your missing data is occurring at random.
* In Missing_Value1 I have showcased how to categorise the missing data.
  - MCAR, MNAR and MAR
  - I have also used Mean/ Median/ Mode Imputation.
  - Mean/ Median / Mode imputation has the assumption that the data are missing completely at random(MAR) I solve this by replacing the NaN with the most fequent occurace of the variables
* In Missing_Value2 I have used Random Sample Impuataion.
   - Random sample imputation consists of taking random observation from the dataset and we use this obseravtion to replace the nan values.
   - It assumes that the data are missing completely at random(MCAR)

# Types of missing data

There are three categories of scenarios for missing data:
1. Missing completely at random (MCAR): The probability of data being missing is equal for all possible data points.
2. Missing at random (MAR): The probability of data being missing is not equal across all data points, but within known classes of data, the probability of missing data is equal. 
3. Missing not at random (MNAR): The probability of data being missing is not equal across all data points, and there is no known grouping of data within which missing data is equally probable.

[(Back to top)](#table-of-contents)

# Imputation Methods

1. Mean/ Median / Mode imputation:
- These are the simplest imputation methods, and, at most, involve calculating some simple column statistics. For each column, and potentially within each group in a MAR scenario, you replace missing values with either a constant value or some column statistic on the available feature values (e.g. the mean or median).
2. Regression imputation:
- A more complex method of imputing data involves building a predictive model that can infer the values of missing data. These methods are more powerful, nd are able to understand the underlying structure of the data in order to provide more intelligent guesses for missing data. So, for example, if we have 5 features and 1 missing, we build a model that predicts the missing 1 given the other 5. One caveat of this method is that it can artificially strengthen relationships in your data, and produce “too good to be true” estimations that simply reinforce the biases and correlations in your data-set. Therefore, these imputed values may underestimate the variance in your data-set.
3. Multiple imputation:
- This method is a way to create more robust estimates for imputed values, and may leverage the above two methods. In multiple imputation, you create N different versions of the imputed data-set, and then pool together the N values in order to produce a final data-set (either by something simple like averaging, or some more complex statistical method). The results of multiple imputation will be less biased than those of single imputation, and better represent the variance of the data-set.
       
[(Back to top)](#table-of-contents)

[GNU General Public License version 3](https://opensource.org/licenses/GPL-3.0)
