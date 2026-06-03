# What Does It Truly Take to Create a Viral Post?

A statistical analysis of social media engagement using linear and logistic regression, built as part of STAT 207 at the University of Illinois Urbana-Champaign.

---

## Overview

Everyone wants to know how to go viral. This project attempts to answer that question through data, using a dataset of 5,000+ social media posts across TikTok, YouTube, and Twitter. The analysis explores what factors predict view counts and high engagement using two regression models.

---

## Research Questions

**Linear Regression**
- How do likes, comments, shares, region, and platform affect the predicted number of views a post receives?
- What is the relationship between likes and views, holding all other variables constant?

**Logistic Regression**
- How do platform, region, content type, views, comments, likes, and shares affect the log-odds of a post having high engagement?

---

## Dataset

- 5,000+ social media posts (TikTok, YouTube, Twitter)
- Unit of observation: individual post
- Key variables: Views, Likes, Comments, Shares, Platform, Region, Content_Type, Engagement_Level

---

## Methods

- Train/test split (80/20, random state = 5)
- OLS linear regression via `statsmodels`
- Logistic regression via `statsmodels`
- Model evaluation: R², RMSE, AUC, confusion matrix, fitted vs. residuals plot, QQ plot, ROC curve

---

## Key Findings

- The linear model produced an R² of just 0.5%, meaning the predictors explained almost none of the variability in view counts
- The RMSE on test data was approximately 1,461,537, indicating poor predictive accuracy
- The logistic model's AUC was 0.5, equivalent to random guessing
- The classifier predicted every post as not having high engagement, yielding 0% sensitivity
- Neither model performed well, suggesting the dataset may lack strong signal between these variables

---

## Limitations

- Likely multicollinearity between likes, views, comments, and shares
- Synthetic dataset may not reflect real-world social media dynamics
- Normality assumption was violated (S-curve in QQ plot), limiting inference reliability

---

## Tech Stack

- Python
- pandas
- statsmodels
- scikit-learn
- matplotlib

---

## File Structure

```
project_03_template.ipynb   # Full analysis notebook
socialmedia.csv             # Dataset
```

---

## Author

Dean Xoubi  
University of Illinois Urbana-Champaign  
Gies College of Business
