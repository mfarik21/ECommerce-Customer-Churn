# **Machine Learning Model for Predicting E-Commerce Customer Churn**

Welcome to the Capstone 3 project for Purwadhika's Digital Talent Incubator (DTI) Data Science program. In this project, we aim to explore and implement the most effective machine learning models for predicting customer churn using the E-commerce Customer Churn Dataset.

## **Included in This Repo**
1. Notebook for analysis and training (`e-commerce-customer-churn.ipynb`)
2. Notebook for deployment (`model-predict.ipynb`)
3. Requirement file for deployment (`requirements.txt`)
4. New observation for deployment prediction (`dataset/new_observation.csv`)
5. Presentation (`Presentation.pdf`)

## **Summary of Notebook**

### **Business Understanding**

#### **Context**
In the highly competitive E-Commerce sector, retaining existing customers is crucial for sustaining business growth and reducing acquisition costs. Identifying potential churners and developing effective retention strategies are essential for maintaining customer loyalty. Machine learning provides valuable insights into customer behavior, helping predict and address churn risks.

#### **Problem Statements**
1. What customer characteristics indicate potential churn?
2. Which machine learning models can effectively predict customer churn for the company?
3. How can machine learning optimize customer retention while minimizing acquisition costs?

#### **Objectives**
1. Identify factors contributing to customer turnover.
2. Develop predictive machine learning models to detect at-risk customers.
3. Optimize customer retention strategies using the best model.

### **Analysis Summary**
- Churning customers have a median tenure of 3 years, compared to 9 years for non-churning ones, with churn rates decreasing over a decade. Among customers with 5 years or less tenure, churning customers are half the number of non-churning ones.
- Complained customers exhibit higher churn rates than those who haven't complained.
- Customers receiving lower cashback amounts have higher churn rates compared to those receiving higher cashback amounts.

### **Modeling**

#### **Best Model**
| Model                                         | F2-Score |
|-----------------------------------------------|----------|
| XGBoost with Random Under Sampling            | 0.77     |
| Weighted XGBoost                              | 0.82     |
| Decision Tree with Random Under Sampling      | 0.76     |
| Weighted Decision Tree                        | 0.68     |

### **Conclusion & Recommendation**

#### **Conclusion and Key Findings**

**Predictive Power:** Leveraging the XGBoost with an F2 Score of 0.82, we can confidently identify potential churning customers at an 82% accuracy rate.

**Financial Impact:** Implementing the predictive model leads to significant cost savings, reducing Customer Acquisition Cost (CAC) by 59%. Projected savings amount to USD 4,770.

**Strategic Advantage:** The proactive loyalty promotion program not only retains customers but also optimizes resource allocation, ensuring a competitive edge in the e-commerce market.

**Best Model:** The best model for this case is the XGBoost Classifier with an F2 Score of 0.82. This model predicts potential churning customers with 82% confidence and reduces potential loss from customer acquisition costs (CAC) by 59% compared to business as usual.

#### **Recommendation**

**Leverage a proactive approach to retain existing customers:**
- Offer loyalty promotion programs to customers predicted to be churning by the model.
- Actively resolve customer complaints, as the EDA indicates that customers who churn are more likely to have complaints.
- Consider increasing the cashback amount for churning customers, as average cashback values for these customers are lower than for non-churning customers.

**Apply machine learning prediction as the base for customer retention policy:**
- Apply the model to new customers to predict potential churning customers.
- Retrain the model periodically to maintain performance.
