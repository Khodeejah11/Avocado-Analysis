\# **Avocado Price Analysis \& Predictive Modeling**



This repository contains a comprehensive data science project focused on predicting avocado prices, analyzing regional market trends, and classifying product types. The project demonstrates a complete data pipeline—spanning data cleaning, long-form data restructuring, exploratory data analysis (EDA), time-series forecasting, and machine learning in Python.



\## **Project Objective**

The goal of this project is to identify the primary drivers of avocado prices across different regions and seasons, and to build robust predictive and classification frameworks using regression, time-series, and dimensionality reduction techniques.



\## **Key Drivers of Avocado Prices**

The exploratory analysis revealed that avocado pricing is driven by a complex interaction of four primary factors:

1. \*\*Type (Organic vs. Conventional):\*\* Organic avocados consistently command premium prices due to higher production costs.

2\. \*\*Supply Dynamics:\*\* Price is inversely related to total volume; higher supply volumes predictably drive down retail prices.

3\. \*\*Seasonality \& Region:\*\* Strong temporal fluctuations occur month-over-month, while specific geographic locations maintain higher baselines regardless of volume.

4\. \*\*Product Segmentation:\*\* Transforming the dataset from a wide to a long format exposed critical pricing variations hidden within specific PLU codes and packaging formats.



\## **Model Development \& Key Insights**



\### 1. **Price Forecasting: Time-Series vs. Linear Regression**

I progressively built four \*\*Linear Regression\*\* models, with Model 4 achieving the lowest error rates and highest $R^2$ among the regression attempts. 



However, when compared to \*\*Time-Series Analysis\*\*, the time-series framework significantly outperformed regression by achieving a lower Root Mean Squared Error (RMSE).

\*   \*\*Model Selection:\*\* An \*\*AR(1)\*\* model was compared against an \*\*AR(2)\*\* model. 

\*   \*\*Finding:\*\* The AR(1) model demonstrated statistical significance ($p < 0.05$) with lower AIC and BIC scores, making it the most reliable tool for forecasting market trends.



\### 2. **Type Classification: Manual Selection vs. PCA**

I evaluated two distinct approaches to predict whether an avocado was Organic or Conventional:

\*   \*\*Approach A (Manual Feature Selection):\*\* A Logistic Regression model built using domain knowledge (Region, Volume, and Season).

\*   \*\*Approach B (Dimensionality Reduction):\*\* Using Principal Component Analysis (PCA) to extract mathematical components.



\*\*Results \& Critical Thinking Insight:\*\*

The manual feature selection model outperformed the PCA approach, yielding higher accuracy and excellent generalization without overfitting (15,300 True Positives; 14,855 True Negatives). 



\*   \*\*The "Premium Pricing" Market Effect:\*\* The model produced 1,642 false positives (misclassifying conventional avocados as organic). Rather than a weakness in the code, this reflects \*\*real-world market behavior\*\*. During peak seasons or in high-demand regions, conventional avocado prices spike to premium levels, making them statistically indistinguishable from organic ones.





\## Repository Structure

&#x20;avocado\_analysis.ipynb  # Full notebook containing EDA, data restructuring, and modeling

&#x20;README.md                # Project documentation

