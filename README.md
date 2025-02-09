# Ad Campaign Performance Analysis

## Project Overview

This project analyzes the performance of two advertising platforms, **Facebook Ads** and **AdWords Ads**, to determine which platform is more effective in terms of **conversions**, **clicks**, and **cost-effectiveness**. The dataset includes daily data for the entire year of 2019, with metrics such as ad views, clicks, conversions, cost per ad, click-through rate (CTR), and cost per click (CPC).

## Research Question

**Which ad platform is more effective in terms of conversions, clicks, and overall cost-effectiveness?**

## Key Metrics Analyzed

- **Conversions**: Number of desired actions driven by the ad.
- **Clicks**: Number of user engagements.
- **Cost-effectiveness**: ROI in terms of cost per click (CPC) and cost per conversion.

## Code and Analysis

### Importing Libraries

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np
from sklearn.linear_model import LinearRegression
from sklearn.metrics import r2_score, mean_squared_error
from statsmodels.tsa.seasonal import seasonal_decompose
from statsmodels.tsa.stattools import coint
import scipy.stats as st
from tabulate import tabulate
```

### Data Preparation

```python
df = pd.read_csv("marketing_campaign.csv")
df['Date'] = pd.to_datetime(df['Date'])
```

### Comparing Campaign Performance

We compared the performance of Facebook and AdWords campaigns using histograms for clicks and conversions.

```python
plt.figure(figsize=(20, 10))
# Facebook Ad Clicks
plt.subplot(2, 4, 1)
sns.histplot(df['Facebook Ad Clicks'], bins=7, edgecolor="k", kde=True, color='skyblue')
# Facebook Ad Conversions
plt.subplot(2, 4, 2)
sns.histplot(df['Facebook Ad Conversions'], bins=7, edgecolor="k", kde=True, color='lightgreen')
# AdWords Ad Clicks
plt.subplot(2, 4, 3)
sns.histplot(df['AdWords Ad Clicks'], bins=7, edgecolor="k", kde=True, color='salmon')
# AdWords Ad Conversions
plt.subplot(2, 4, 4)
sns.histplot(df['AdWords Ad Conversions'], bins=7, edgecolor="k", kde=True, color='gold')
plt.show()
```

### Conversion Categories

We categorized conversions into different ranges to analyze the frequency of high and low conversion days.

```python
def create_conversion_category(conversion_col):
    category = []
    for conversion in df[conversion_col]:
        if conversion < 6:
            category.append('less than 6')
        elif conversion < 11:
            category.append('6 - 10')
        elif conversion < 16:
            category.append('10 - 15')
        else:
            category.append('more than 15')
    return category

df['Facebook Conversions Category'] = create_conversion_category('Facebook Ad Conversions')
df['AdWords Conversions Category'] = create_conversion_category('AdWords Ad Conversions')
```

### Correlation Analysis

We analyzed the correlation between ad clicks and conversions for both platforms.

```python
facebook_corr = df[['Facebook Ad Conversions','Facebook Ad Clicks']].corr()
adwords_corr = df[['AdWords Ad Conversions','AdWords Ad Clicks']].corr()
print('Correlation Coeff \n--------------')
print('Facebook :',round(facebook_corr.values[0,1],2))
print('AdWords : ',round(adwords_corr.values[0,1],2))
```

### Hypothesis Testing

We tested the hypothesis that Facebook ads result in more conversions than AdWords ads.

```python
t_stats, p_value = st.ttest_ind(a = df['Facebook Ad Conversions'], b = df['AdWords Ad Conversions'], equal_var = False)
if p_value < 0.05:
    print("\np-value is less than significance value, Reject the null hypothesis")
else:
    print("\np-value is greater than significance value, Accept the null hypothesis")
```

### Regression Analysis

We performed a linear regression to predict Facebook ad conversions based on clicks.

```python
X = df[['Facebook Ad Clicks']]
y = df[['Facebook Ad Conversions']]
reg_model = LinearRegression()
reg_model.fit(X,y)
prediction = reg_model.predict(X)
r2 = r2_score(y, prediction)*100
mse = mean_squared_error(y, prediction)
print('Accuracy (R2 Score):',round(r2,2),'%')
print('Mean Squared Error:', round(mse,2))
```

### Time Series Analysis

We analyzed weekly and monthly trends in conversions and cost per conversion (CPC).

```python
df['month'] = df['Date'].dt.month
df['week'] = df['Date'].dt.weekday
weekly_conversion = df.groupby('week')[['Facebook Ad Conversions']].sum()
monthly_conversion = df.groupby('month')[['Facebook Ad Conversions']].sum()
```

### Cointegration Test

We tested for a long-term equilibrium relationship between ad spend and conversions.

```python
score, p_value, _ = coint(df['Cost per Facebook Ad'], df['Facebook Ad Conversions'])
if p_value < 0.05:
    print("\np-value is less than significance value, Reject the null hypothesis")
else:
    print("\np-value is greater than significance value, Accept the null hypothesis")
```

## Key Findings

1. **Facebook outperformed AdWords** in terms of higher conversion days.
2. **Strong positive correlation** between clicks and conversions on Facebook.
3. **Higher mean conversions** on Facebook compared to AdWords.
4. **Weekly and monthly trends** showed consistent engagement, with some seasonal fluctuations.
5. **Cost per conversion (CPC)** was relatively stable, with lower values in May and November.

## Recommendations

- **Reallocate resources** towards Facebook ads due to higher conversion rates.
- **Optimize AdWords campaigns** to improve conversion rates.
- **Leverage time-based trends** to maximize ROI during high-performing periods.

## Conclusion

Facebook ads are more effective in driving conversions compared to AdWords. Businesses should focus on optimizing Facebook campaigns and consider reallocating budgets to maximize ROI.

---

**Note:** Images and visualizations are to be inserted in the appropriate sections as indicated in the code.
