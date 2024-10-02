# Warranty Claims Fraud Prediction
![](https://www.genre.com/content/dam/generalreinsuranceprogram/images/hero-publications/key-takeaways-from-our-us-claims-fraud-survey-en-pubhero.jpg/_jcr_content/renditions/cq5dam.crop.610.610.jpeg)
## Project Overview
The aim of this project is to analyze warranty claims by region, product type, claim value, and other key features to predict their authenticity. 
The dataset used for this project was sourced from Kaggle 

## Data Dictionary
| Column Name         | Description                                     |
|---------------------|-------------------------------------------------|
| Unnamed: 0          | Index                                           |
| Region              | Region of the claim                             |
| State               | State of the claim                              |
| Area                | Area of the claim                               |
| City                | City of the claim                               |
| Consumer_profile    | Consumer profile (Business/Personal)            |
| Product_category    | Product category (Household/Entertainment)      |
| Product_type        | Product type (AC/TV)                            |
| AC_1001_Issue       | Issue with AC component 1 (0 - No issue/No component, 1 - repair, 2 - replacement) |
| AC_1002_Issue       | Issue with AC component 2 (0 - No issue/No component, 1 - repair, 2 - replacement) |
| AC_1003_Issue       | Issue with AC component 3 (0 - No issue/No component, 1 - repair, 2 - replacement) |
| TV_2001_Issue       | Issue with TV component 1 (0 - No issue/No component, 1 - repair, 2 - replacement) |
| TV_2002_Issue       | Issue with TV component 2 (0 - No issue/No component, 1 - repair, 2 - replacement) |
| TV_2003_Issue       | Issue with TV component 3 (0 - No issue/No component, 1 - repair, 2 - replacement) |
| Claim_Value         | Claim value in INR                              |
| Service_Center      | Service center code                             |
| Product_Age         | Product age in days                             |
| Purchased_from      | Purchased from (Dealer, Manufacturer, Internet) |
| Call_details        | Call duration                                   |
| Purpose             | Purpose of the call                             |
| Fraud               | Fraudulent (1) or Genuine (0) Conclusion       |

## Conclusion
From the exploratory data analysis, it was found that:
- Warranty claims are most frequent in the southern region of India, particularly in Andhra Pradesh and Tamil Nadu.
- Fraudulent claims are more common in urban regions such as Hyderabad and Chennai.
- The dataset includes claims for two products: TVs and ACs. TVs have higher warranty claims when purchased for personal use compared to ACs.
- Fraudulent claims for ACs occur even when there are no issues with the AC parts.
- Fraudulent claims for TVs can occur with or without issues in the TV parts.
- Fraudulent claims are more frequent when purchases are made through the manufacturer.
- Fraudulent claims tend to have higher claim values compared to genuine claims.
- Service center 13 had the highest number of fraudulent claims despite having fewer total warranty claims.
- Fraudulent claims are more frequent when the customer care call duration is less than or equal to 3 minutes.
  
## Recommendation
- A Focus on High-Risk Regions: Implement stricter verification and monitoring processes for warranty claims originating from Andhra Pradesh and Tamil Nadu, especially in urban areas like Hyderabad and Chennai.
- Investigate Service Center 13:  As it has a disproportionately high number of fraudulent claims.
- Manufacturer Sales Monitoring: Strengthen fraud detection measures for claims associated with purchases made directly through manufacturers.
- Leverage Customer Call Duration: Use the observed correlation between call duration and fraud to flag suspicious claims. Claims with call durations of 3 minutes or under, could trigger additional verification steps.
- Regular Audits and Process Adjustments: Periodically review claim handling processes, particularly for high-value claims, and monitor for evolving fraud patterns.

#### Machine Learning Models:
Finally, for the machine learning models, I have used three models - Logistic Regression, Decision Tree Classifier, and Random Forest Classifier. The Random Forest Classifier has the highest accuracy( 90%), F1 Score (89%), and the lowest mean squared error, and mean absolute error. <br>
Therefore, the Random Forest Classifier is a good fit for predicting fraudulent warranty claims and can be improved further by Increasing the size of the dataset, particularly adding more examples of fraudulent claims, would likely improve model recall and allow for better detection of fraud


