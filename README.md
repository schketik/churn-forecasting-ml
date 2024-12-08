
# **Customer Churn Prediction for Telecom**

## **Overview**  
This project aims to predict customer churn for a telecommunications company, enabling the business to proactively identify at-risk customers and take appropriate retention measures. Using machine learning techniques, we build a predictive model and analyze critical factors contributing to customer churn.  

---

## **Project Objectives**  
1. Develop a machine learning model to predict customer churn.  
2. Analyze factors influencing customer behavior and churn.  
3. Provide actionable business recommendations for customer retention.  

---

## **Dataset**  
The project uses four datasets:  
- `contract_new.csv`: Information about customer contracts (e.g., type, duration, and payment method).  
- `personal_new.csv`: Demographic data of customers.  
- `internet_new.csv`: Details about internet services used by customers.  
- `phone_new.csv`: Information about telephony services.  

---

## **Pipeline**  
1. **Data Preprocessing**:  
   - Handling missing values and duplicates.  
   - Encoding categorical features and scaling numerical features.  
2. **Feature Engineering**:  
   - Created new features (`duration`, `churn`) to enhance prediction.  
3. **Model Training**:  
   - Used various machine learning algorithms, with **LGBMClassifier** selected as the best-performing model.  
   - Conducted hyperparameter optimization using `RandomizedSearchCV`.  
4. **Model Evaluation**:  
   - Evaluated using metrics such as **ROC-AUC**, precision, recall, and F1-score.  
5. **Feature Importance**:  
   - Used **SHAP** for interpretability and to identify key factors driving churn.  

---

## **Key Findings**  
1. **Model Performance**:  
   - The **LGBMClassifier** achieved a high ROC-AUC score of **0.902** on the test set.  
2. **Important Features**:  
   - Contract type and duration were the most significant predictors of churn.  
   - Engagement with additional services (e.g., `StreamingTV`, `DeviceProtection`) reduced churn likelihood.  
   - Demographic factors, such as having a partner, also influenced churn behavior.  

---

## **Business Recommendations**  
1. Proactively target customers with month-to-month contracts using loyalty programs or discounts for long-term plans.  
2. Offer promotions or free trials for additional services to increase engagement.  
3. Monitor customers with high monthly charges and provide tailored packages.  
4. Enhance technical support services to improve customer satisfaction and reduce churn.  

---

## **Technologies Used**  
- **Programming Language**: Python  
- **Libraries**:  
  - pandas, numpy, matplotlib, seaborn  
  - scikit-learn, lightgbm  
  - SHAP for feature importance analysis  

---

## **How to Use**  
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Customer-Churn-Prediction.git
   ```
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the project notebook:
   ```bash
   jupyter notebook Churn_Prediction.ipynb
   ```

---

## **Future Work**  
1. Address class imbalance using techniques like **SMOTE**.  
2. Incorporate additional data sources, such as customer feedback.  
3. Test on updated datasets and monitor performance over time.  

