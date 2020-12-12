**Life Expectancy Prediction using Linear Regression**

**Aim:**

The main aim of the project is to predict the life expectancy of people
according to various parameters.

**Data:**

The dataset consisted of 22 columns and 2056 rows. The different columns
were as follows:

![image](https://i.ibb.co/0mpZNMZ/image.png)

**Cleaning Dataset:**

a.  Null Values

![](https://i.ibb.co/Kh50Y7w/image.png)

> For cleaning nulls, two methods were used: imputation, grouped mean
> and dropping.

1.  Imputation

    For columns like Schooling, Alcohol, Income, BMI, Population,
    thinness, columns which were positively correlated to these columns
    were used to understand corresponding missing values.

2.  Group mean

    The columns which did not have a robust visible correlation were
    filled according to the mean of the values grouped by country. If
    the number of nulls of a given group is less than 10, the entire
    column\'s mean was used as filler.

3.  Dropping

    Specific columns, like Life expectancy and Adult Mortality, has a
    low number of nulls, and thus, they were dropped.

<!-- -->

b.  Outliers

> Zscore for values from columns was calculated; if the Z-score\'s
> absolute value was more significant than the threshold, it was
> replaced with the country mean.

**Exploratory Data Analysis:**

Boxplots of all the columns,

![A picture containing shoji, building Description automatically
generated](https://i.ibb.co/F6KSWkb/download.png)


HeatMap between different values,

![](https://i.ibb.co/g3xS1mb/image.png)

It can be observed that there are a few very high positive correlation,
like \'Expenditure\' and \'GDP\'.

For Life expectancy, \'Schooling\' and \'Income composition of
resources\' are very high.

Important Distribution Plots:

![](https://i.ibb.co/sqckptT/image.png)

![](https://i.ibb.co/b1XpPRV/image.png)

![](https://i.ibb.co/0BfnPm3/image.png)

PairPlot of the dataset:

![](https://i.ibb.co/Cs9HBVn/download.png)

The image can be seen at <https://ibb.co/BK6CLTg>

From the image, we can see that mane values are linearly dependant.

The target variable, \'Life expectancy\', is linearly related to
\'Income composition\', \'Schooling\',\' HIV/Aids\', and \'Adult
Mortality\'.

These features will be an essential factor in the model.

**Model 1 (Baseline Model)**

Task: Regression

Library: Weka

Algorithm: Linear Regression

**R2 Score: 0.7663755802699652 (Test)**

For the baseline model, the features chosen were,

\'Adult Mortality\',

\'Alcohol\',

\' BMI \',

\'under-five deaths \',

\'Polio\',

\' HIV/AIDS\',

\' thinness 1-19 years\',

\'Schooling\',

\'Income composition of resources\'

![](https://i.ibb.co/9sm00wd/image.png)

**Model 2**

Task: Regression

Library: Weka

Algorithm: Random Forest

**R2 Score: 0.9494861514474349 (Test)**

The features that were used were:

Adult Mortality\',

\'Alcohol\'

\' BMI \',

\'under-five deaths \'

\'Polio\',

\' HIV/AIDS\',

\' thinness 1-19 years\',

\'infant deaths\',\'Schooling\',

\'Total expenditure\',

\'Measles \',

\'Diphtheria \',

\'Income composition of resources\'

![](https://i.ibb.co/gMdttW4/image.png)

**Model 3**

Task: Regression

Library: Weka

Algorithm: Random Forest

**R2 Score: 0.9535801444908933 (Test)**

The features used were

\'Income composition of resources\',

\'Schooling\'

\' thinness 1-19 years\',

\' HIV/AIDS\',

\'Adult Mortality\'

![](https://i.ibb.co/qFSzLsV/image.png)

**Model 4**

Task: Regression

Library: Weka

Algorithm: Random Forest

**R2 Score: 0.962142599298509 (Test)**

The features used were,

\'Measles \',

\'percentage expenditure\',

\'infant deaths\',

\'Diphtheria \',

\'Total expenditure\',

\'Population\',

\' HIV/AIDS\',

\'Schooling\',

\'Hepatitis B\'

![](https://i.ibb.co/FX0Vwpz/image.png)

**Model 5**

Task: Regression

Library: Weka

Algorithm: Random Forest

**R2 Score: 0.9673519085487334 (Test)**

Parameters used for the model are,

\'Adult Mortality\',

\'Hepatitis B\',

\' thinness 1-19 years\',

\' HIV/AIDS\',\'Diphtheria \',

\'Income composition of resources\',

\'infant deaths\',

\'Alcohol\'

![](https://i.ibb.co/d4fJZWG/image.png)

**Model 6**

Task: Regression

Library: Weka

Algorithm: Random Forest

**R2 Score: 0.9702330510703981 (Test)**

The parameters used were,

\'Adult Mortality\',

\'Hepatitis B\',

\' thinness 1-19 years\',

\'Year\',

\'under-five deaths \',

\'Polio\',

\' HIV/AIDS\',

\'Diphtheria \',

\'Income composition of resources\',

\'infant deaths\',

\'Alcohol\'

![](https://i.ibb.co/wcCGLPP/image.png)

**Summary:**

First, the dataset was cleaned and scaled. For scaling min-max scaler
was used.

All the outliers were removed, using three different techniques,
imputation, grouped mean and dropping.

Specific attributes were found to be highly correlated to the target
variable, which was \'Life Expectancy\'.

Models were built by tweaking the parameters, to receive the highest
accuracy.

The highest accuracy reached was 97.02% on test data.

**Future works:**

1.  Deploying the model

    -Deploying the model will be a huge step, making interactions
    between the model and end-user easier. Additional data can also be
    collected.

2.  Use of better algorithms

    -The only algorithms used are RandomForest and LinearRegression;
    checking other algorithms will benefit.

3.  Trying to improve imputation

    -Since there are many null values, a better way to fill in those
    values may result in higher accuracy.

**Business Idea:**

The project can be used in two different domains: the healthcare domain
and the insurance company.

1.  Healthcare Domain:

    In the healthcare domain, the model can help governments and
    hospitals understand the significant features that affect life
    expectancy and how it can be handled. The government can conduct
    specific awareness programs for better life expectancy.

2.  Insurance Company:

    Insurance companies can plan their packages based on the life
    expectancy of individuals. Different kinds of offers and packages
    can be given accordingly so that the person buys it.
    
    
    **Contributors**

    ThomasKutty Reji


    Ipshita Ghosh
