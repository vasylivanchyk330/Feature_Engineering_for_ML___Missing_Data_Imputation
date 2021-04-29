Brief Review

Imputation is the act of replacing missing data with statistical estimates of the missing values. The goal of any imputation technique is to produce a complete dataset that can be used to train machine learning models.

ARBITRARY VALUE IMPUTATION: <br>
Arbitrary value imputation consists of replacing all occurrences of missing values (NA) within a variable by an arbitrary value. Typically used arbitrary values are 0, 999, -999 (or other combinations of 9s) or -1 (if the distribution is positive).

COMPLETE CASE ANALYSIS: <br>
Complete-case analysis (CCA), also called "list-wise deletion" of cases, consists in discarding observations where values in any of the variables are missing. Complete Case Analysis means literally analysing only those observations for which there is information in all of the variables in the dataset.

END OF DISTRIBUTION IMPUTATION: <br>
It is an automation of arbitrary value imputation by selecting arbitrary values at the end of the variable distributions.

FREQUENT CATEGORY IMPUTATION: <br>
Mode imputation consists of replacing all occurrences of missing values (NA) within a variable by the mode, which in other words refers to the most frequent value or most frequent category.

MEAN / MEDIAN IMPUTATION: <br>
Mean / median imputation consists of replacing all occurrences of missing values (NA) within a variable by the mean (if the variable has a Gaussian distribution) or median (if the variable has a skewed distribution).

ARBITRARY VALUE IMPUTATION FOR CATEGORICAL VARIABLES: <br>
This is the most widely used method of missing data imputation for categorical variables. This method consists in treating missing data as an additional label or category of the variable. All the missing observations are grouped in the newly created label 'Missing'. This is in essence, the equivalent of replacing by an arbitrary value for numerical variables. It does not assume anything about the fact that the data is missing. It is very well suited when the number of missing data is high.

ADDING A VARIABLE TO CAPTURE NA: <br>
If data are not missing at random, it is a good idea to replace missing observations by the mean / median / mode AND flag those missing observations as well with a Missing Indicator. A Missing Indicator is an additional binary variable, which indicates whether the data was missing for an observation (1) or not (0).
Commonly used together:
- Mean / median imputation + missing indicator (Numerical variables)
- Frequent category imputation + missing indicator (Categorical variables)
- Random sample Imputation + missing indicator (Numerical and categorical)

RANDOM SAMPLE IMPUTATION: <br>
Random sampling consists of taking a random observation from the pool of available observations of the variable and using that randomly extracted value to fill the NA. In random sample imputation, one takes as many random observations as missing values are present in the variable.
By random sampling observations of the variable for those instances where data is available, it is guaranteed that the mean and standard deviation of the variable, preserved, and the frequency of the different categories/labels within the variable are preserved. Well suited for linear models as it does not distort the distribution, regardless of the % of NA.
