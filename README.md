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


### Data Preparation

<img width="708" alt="image" src="https://github.com/user-attachments/assets/8e85fc5f-b2bc-4b9b-a6d4-e9a9514f652e" />


### Comparing Campaign Performance

We compared the performance of Facebook and AdWords campaigns using histograms for clicks and conversions.

![image](https://github.com/user-attachments/assets/fd1068b1-cbec-49fe-9e86-b796db68564e)


### Conversion Categories

We categorized conversions into different ranges to analyze the frequency of high and low conversion days.

<img width="137" alt="image" src="https://github.com/user-attachments/assets/41f87156-df79-4948-bb2e-93ff3e3f8f57" />

![image](https://github.com/user-attachments/assets/9a11afc1-f168-4f56-bb4d-19291f39c88d)

```

### Correlation Analysis

We analyzed the correlation between ad clicks and conversions for both platforms.

![image](https://github.com/user-attachments/assets/e06ab02d-ae0e-492b-8096-4325fc0f467d)

<img width="110" alt="image" src="https://github.com/user-attachments/assets/62a80364-8994-4af8-ab30-d34e31af2bdc" />

### Hypothesis Testing

We tested the hypothesis that Facebook ads result in more conversions than AdWords ads.

<img width="398" alt="image" src="https://github.com/user-attachments/assets/12a4d137-7ff8-4480-b0b5-750ed0eb18d5" />


### Regression Analysis

We performed a linear regression to predict Facebook ad conversions based on clicks.

![image](https://github.com/user-attachments/assets/3b0da3af-197d-418b-b34e-fe7150981361)
<img width="215" alt="image" src="https://github.com/user-attachments/assets/80e61bcf-08e0-46e8-977d-b5b1b3a63473" />
![image](https://github.com/user-attachments/assets/da88ac08-53bf-4a8e-88fb-7c7e0b3c3441)


### Time Series Analysis

We analyzed weekly and monthly trends in conversions and cost per conversion (CPC).

![image](https://github.com/user-attachments/assets/dbb1e83e-1072-4a0f-a49b-d045be42a75b)
![image](https://github.com/user-attachments/assets/70a9d246-ee31-4722-bbc5-7eb0d7e217cf)
![image](https://github.com/user-attachments/assets/d17bdce8-da5e-4e02-9fae-83116217f4ad)



### Cointegration Test

We tested for a long-term equilibrium relationship between ad spend and conversions.

<img width="404" alt="image" src="https://github.com/user-attachments/assets/ede1d8b6-7ebc-404b-8238-45f34dddf9d6" />


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
