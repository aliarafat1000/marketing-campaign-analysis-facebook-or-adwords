# Ad Campaign Performance Analysis

## Project Overview

This project analyzes the performance of two advertising platforms to which a company campaigned their product on, **Facebook Ads** and **AdWords Ads**, to determine which platform is more effective in terms of **conversions**, **clicks**, and **cost-effectiveness**. The dataset includes daily data for the entire year of 2019, with metrics such as ad views, clicks, conversions, cost per ad, click-through rate (CTR), and cost per click (CPC).

## Research Question

**Which ad platform is more effective in terms of conversions, clicks, and overall cost-effectiveness?**

## Key Metrics Analyzed

- **Conversions**: Number of desired actions driven by the ad.
- **Clicks**: Number of user engagements.
- **Cost-effectiveness**: ROI in terms of cost per click (CPC) and cost per conversion.

Table summarizing the skills used in the project:

| **Category**            | **Skills/Tools**                                                                 |
|--------------------------|---------------------------------------------------------------------------------|
| **Data Analysis**        | Exploratory Data Analysis (EDA), Descriptive Statistics                         |
| **Data Visualization**   | Histograms, Scatter Plots, Bar Charts, Line Charts (Matplotlib, Seaborn)        |
| **Statistical Analysis** | Hypothesis Testing (t-tests), Correlation Analysis, Cointegration Test          |
| **Machine Learning**     | Linear Regression, Model Evaluation (R², MSE)                                   |
| **Time Series Analysis** | Weekly/Monthly Trends, Cost Per Conversion (CPC) Trends                         |
| **Libraries**            | Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Statsmodels, SciPy            |
| **Business Insights**    | Data-Driven Decision Making, Resource Allocation, Campaign Optimization         |
| **Reporting**            | Visual Storytelling, Markdown Documentation                                     |


---

# 📊 **Advertising Performance Analysis**  

## **Analysis**  

### **Data Preparation**  
Data was preprocessed to ensure accuracy, consistency, and readiness for analysis. This included handling missing values, formatting dates, and structuring the dataset for visualization and modeling.  

<img width="708" alt="image" src="https://github.com/user-attachments/assets/8e85fc5f-b2bc-4b9b-a6d4-e9a9514f652e" />  

### **Comparing Campaign Performance**  
We compared Facebook and AdWords campaign performance by visualizing the distribution of clicks and conversions. The histograms below reveal differences in user engagement and conversion trends between the two platforms.  

![image](https://github.com/user-attachments/assets/fd1068b1-cbec-49fe-9e86-b796db68564e)  

### **Conversion Categories**  
To better understand conversion patterns, we categorized conversions into different ranges. This helped us identify the frequency of high and low conversion days and provided insights into campaign performance variability.  

<img width="137" alt="image" src="https://github.com/user-attachments/assets/41f87156-df79-4948-bb2e-93ff3e3f8f57" />  

![image](https://github.com/user-attachments/assets/1cb8b761-719c-4b1f-931c-a484b639f280)


### **Correlation Analysis**  
A correlation analysis was conducted to determine the strength of the relationship between ad clicks and conversions for both Facebook and AdWords. The findings indicate a **strong positive correlation (0.87) between Facebook ad clicks and conversions**, meaning that an increase in Facebook ad clicks is strongly associated with higher conversions.  

![image](https://github.com/user-attachments/assets/e06ab02d-ae0e-492b-8096-4325fc0f467d)  
<img width="110" alt="image" src="https://github.com/user-attachments/assets/62a80364-8994-4af8-ab30-d34e31af2bdc" />  

### **Hypothesis Testing**  
We conducted hypothesis testing to verify whether **Facebook ads result in significantly higher conversions than AdWords ads**.  

- **Null Hypothesis (H₀):** No difference in conversions between Facebook and AdWords.  
- **Alternative Hypothesis (H₁):** Facebook ads lead to more conversions than AdWords.  

With a **p-value of 9.35**, we rejected the null hypothesis, confirming that Facebook ads are significantly more effective in driving conversions.  

<img width="398" alt="image" src="https://github.com/user-attachments/assets/12a4d137-7ff8-4480-b0b5-750ed0eb18d5" />  

### **Regression Analysis**  
A linear regression model was developed to predict **Facebook ad conversions based on the number of clicks**. The regression analysis helps estimate how many conversions can be expected from a given number of ad clicks.  

- The model achieved an **R² score of 76.35%**, indicating strong predictive power.  
- The regression line visually represents the relationship between ad clicks and conversions.  

![image](https://github.com/user-attachments/assets/3b0da3af-197d-418b-b34e-fe7150981361)  
<img width="215" alt="image" src="https://github.com/user-attachments/assets/80e61bcf-08e0-46e8-977d-b5b1b3a63473" />  
![image](https://github.com/user-attachments/assets/da88ac08-53bf-4a8e-88fb-7c7e0b3c3441)  

### **Time Series Analysis**  
To understand user engagement over time, we analyzed trends in conversions and **Cost Per Conversion (CPC)** over **weekly and monthly periods**.  

- **Weekly Trends:** Conversion rates remain relatively stable, with the highest engagement on Mondays and Tuesdays.  
- **Monthly Trends:** A steady upward trajectory is observed, with some seasonal fluctuations.  
- **CPC Trends:** Cost per conversion fluctuates but remains stable, with May and November showing the lowest CPC, indicating optimal times for budget allocation.  

![image](https://github.com/user-attachments/assets/dbb1e83e-1072-4a0f-a49b-d045be42a75b)  
![image](https://github.com/user-attachments/assets/70a9d246-ee31-4722-bbc5-7eb0d7e217cf)  
![image](https://github.com/user-attachments/assets/d17bdce8-da5e-4e02-9fae-83116217f4ad)  

### **Cointegration Test**  
To determine if **advertising spend and conversions maintain a long-term equilibrium relationship**, a cointegration test was conducted. The results indicate a **stable proportional impact of ad spend changes on conversions over time**. This suggests that businesses can optimize their spending strategies without significant fluctuations in conversion rates.  

<img width="404" alt="image" src="https://github.com/user-attachments/assets/ede1d8b6-7ebc-404b-8238-45f34dddf9d6" />  

## **Key Findings**  

1. **Facebook Ads significantly outperform AdWords Ads** in conversion rates.  
2. **Strong positive correlation** (0.87) between Facebook ad clicks and conversions.  
3. **Higher average conversions on Facebook** compared to AdWords.  
4. **Weekly and monthly trends show stable engagement**, with Mondays and Tuesdays having the highest conversions.  
5. **Cost Per Conversion (CPC) remains stable**, with lower values in **May and November**, making them cost-effective months for advertising.  

## **Recommendations**  

✅ **Increase Facebook Ad Budget:** Given its **high conversion rates**, businesses should allocate **more resources to Facebook advertising**.  
✅ **Optimize AdWords Performance:** Explore ways to **improve AdWords campaigns**, such as refining audience targeting and testing new ad formats.  
✅ **Leverage Time-Based Trends:** Focus on **high-performing days (Mondays & Tuesdays)** and **low CPC months (May & November)** for maximum ROI.  
✅ **Monitor Ad Spend & Conversions Continuously:** Since **ad spend and conversions have a long-term equilibrium relationship**, businesses should maintain a **data-driven approach to budget allocation**.  

## **Conclusion**  

📢 **Facebook Ads are more effective** than AdWords in driving conversions. Businesses should focus on **optimizing Facebook campaigns** and **reallocating budgets** to **maximize ROI**.  

---

