# Fannie-Mae-Single-Family-Loan-Perforamce-Data-Analysis

## Introduction

The Fannie Mae Single-Family Loan Performance Data is a large dataset released by Fannie
Mae that includes detailed information on the performance of single-family mortgage loans. This
data is made available to help researchers, investors, and analysts better understand mortgage
loan performance and risk, as well as to improve modeling and analytics related to the U.S.
housing market.


## Key Features of the Dataset

- **Loan-Level Data :** It contains detailed data at the individual loan level, which allows for
in-depth analysis.
- **Credit Performance :** The dataset tracks the performance of loans over time, including
delinquency status, credit scores, loan-to-value (LTV) ratios, and other factors that
influence loan performance.
- **Origination Data :** Includes information on the characteristics of the loans when they
were originated, such as interest rates, loan purpose, and property types.
- **Performance Data :** Tracks the performance of the loans on a monthly basis, including
payment history, default status, and modifications
- **Modification Data :** Includes details on any modifications to the original loan terms, such
as changes in interest rates or repayment terms.



## Structure
The dataset is split into two parts:

1. **Aquisition** : This contains static information about the loans at the time they were originated (e.g., credit scores, loan terms).
2. **Performance** : This tracks the monthly performance of each loan, such as delinquency
status, payments made, and loan modifications.



## Data Coverage
The dataset spans from 2000 onwards, covering millions of loans.
It is updated quarterly, ensuring that the data remains relevant and reflects the latest
performance metrics.

***In this project, all the analysis will be done on year 2000 and 2001.***


## Documents Used for Reference

1. [Single-Family Loan Performance Dataset and Credit Risk Transfer - Glossary and File Layout](https://capitalmarkets.fanniemae.com/resources/file/credit-risk/pdf/crt-file-layout-and-glossary.pdf)

2. [Fannie Mae Single-Family Loan Performance Data FAQs](https://capitalmarkets.fanniemae.com/resources/file/credit-risk/pdf/sf-loan-performance-dataset-faqs.pdf)


## Analysis

### 1) Compare the Average FICO Across the Two Years

Borrowers and co-borrowers in 2001 had better credit scores compared to 2000, with a significant increase in both categories by the end of 2001.

Both borrower and co-borrower FICO scores see a sharp rise in October-December 2001, suggesting that either higher credit score borrowers were entering the market, or lending criteria became more selective toward the end of the year.


### 2) The monthly delinquency rates for 30, 60 and 90 days past due and how they vary by loan term

Calculating the monthly delinquency rates for loans that are 30, 60, and 90 days past due for loans originated in 2000 and 2001. Utilizing 'Origination Date' and 'Monthly Reporting Period'.

Formula Used: Delinquency Rate = (number of delinquent loans / total loans) * 100

The rising delinquency rates for 30-day and 60-day past-due loans from 2000 to 2001 suggest that borrowers faced increasing difficulties making payments over time.
The 30-day delinquency rate in particular shows a consistent upward trend, indicating short-term financial struggles among borrowers.


### 3) Stacked bar chart showing the poor, fair good, very good, and excellent credit score with a mortgage per state for first time buyers.

Very Good and Good credit score categories dominate the first-time buyer market in most states.

low proportion of buyers with Excellent credit indicates that only a minority are in the top tier of creditworthiness.

Larger states like California, Texas, and Florida have much larger populations of first-time buyers, which could be reflective of their housing market size and population growth rates.


### 4) Analyze correlations between the FICO Score, LTV Ratio, and Interest Rate with the loan status.

The values in the heatmap range between -1 and 1, where:

1. 1 (or close to it) indicates a strong positive correlation.
2. -1 (or close to it) indicates a strong negative correlation.
3. 0 indicates no correlation.

Observations:
1. FICO Score and Loan Status Correlation: -0.11 (Weak Negative)

As the FICO Score increases, the loan status tends to improve. However, the relationship is not strong, which means that other features are also affecting loan status.

2. LTV Ratio and Loan Status Correlation: 0.04 (Very Weak Positive)

It means that higher LTV ratios (riskier loans) slightly increase the likelihood of delinquency, but it's effect is negligible in our data.

3. Interest Rate and Loan Status Correlation: 0.01 (Not Significant)

It means that interest rate levels do not predict whether a loan will become delinquent or not.

4. FICO Score and LTV Ratio Correlation: -0.10 (Weak Negative)

It means that higher FICO scores are generally associated with lower LTV ratios, but the relationship between them is weak in our data.

5. FICO Score and Interest Rate Correlation: -0.12 (Weak Negative)

Higher FICO scores usually tend to correlate with slightly lower interest rates. However, this relationship in our data is not very strong.

6. LTV Ratio and Interest Rate Correlation: 0.09 (Weak Positive)

It means that loans with higher LTV ratios tend to have slightly higher interest rates.


### 5) Distribution of FICO Scores, LTV Ratios, and Interest Rates across different loan statuses (performing, delinquent, defaulted).

Interpretation for FICO Score Distribution across Loan Statuses

Higher FICO scores (>700) are predominantly associated with performing loans, which indicates that borrowers with good credit are less likely to default on their loans.

Interpretation for LTV Ratios Distribution across Loan Statuses

The LTV ratio plays a role in determining loan performance, with higher LTV ratios being slightly more likely to be delinquent.

Loans with an LTV ratio close to or above 80% have a higher risk of delinquency, but many of these loans are still performing.

Interpretation for Interest Rates Distribution across Loan Statuses

Performing Loans dominate the distribution, particularly around the 8% interest rate mark, which appears to be the most common interest rate for performing loans whereas Delinquent Loans (yellow) are present but in much smaller numbers across the interest rate spectrum. However, they are visible at various interest rates.


### Compare default rates for loans originated in different quarters to assess if default risk has changed over time.

Formula used:

Default Rate = (Defaulted Loans / Total Loans) * 100

2000 shows a steady rise in default rates, peaking in Q4 2000 with a default rate of 0.0078%.

2001 shows more fluctuations in default rates across quarters, with a drop in defaults by Q4 2001.

The overall default rates are very low, indicating a stable loan portfolio with minimal risk of default during these years.


### The percentage of the loan amount recovered after default, through foreclosure or other means.

Formula used:

Recovery Percentage = (Total_Recovered_Amount/ Original_Loan_Amount) * 100

The percentage of the loan amount recovered after default, through foreclosure or other
means is 25%.


### Plot average, median, and variance of property price changes over the entire duration, bucketed by month.

Interpretation of Results for Average Property Price

2000: The average price starts relatively low around $105,000 and gradually increases over the months, showing a steady rise until the end of the year.

2001: The average price begins at a higher level, peaking in February 2001 at $124,000, and then declines for the remainder of the year.

It means that the rising prices during 2000 suggest a growing housing market, while the decline in 2001 may indicate changes in the market such as cooling demand.

Interpretation of Results for Median Property Price

Similar to the average, the median property price starts lower in 2000 (around $95,000), and increases throughout the year.

However, in 2001, the median price remains more stable, with a less pronounced peak in February 2001 before a moderate decline.

The median price being lower than the average in most months suggests that the distribution of property prices is skewed, with higher-priced properties pulling up the average.

This means that the majority of properties are priced below the average, and a few high-value properties are driving the higher average.

Interpretation of Results for Price Variance

The high variance in property prices indicates a broad range of property values, with some properties priced significantly higher than others.

The decline in variance toward the end of 2001 suggests that property prices may be becoming more homogeneous, with less variation between high-end and low-end properties.