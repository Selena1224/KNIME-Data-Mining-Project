# Predicting Hiring Decisions Using Machine Learning in KNIME  

## 1. Project Overview  
This project applies machine learning techniques in KNIME to predict hiring decisions based on candidate attributes such as experience, education, and training hours. The goal is to develop a data-driven approach to hiring, improving efficiency and reducing bias in recruitment.

## 2. Dataset  
- **Source:** [Kaggle - HR Analytics: Job Change of Data Scientists](https://www.kaggle.com/datasets)  
- **Records:** 14,000+ job seeker profiles  
- **Features Used:**  
  - Experience Level: Total years in relevant roles  
  - Education: Highest degree attained (Bachelor’s, Master’s, PhD)  
  - Training Hours: Time spent on upskilling programs  
  - City Development Index: Economic development of the candidate’s location  
  - Company Size: Size of the candidate’s most recent employer  
  - Target Variable: Whether the candidate was hired (1) or not hired (0)  

## 3. Data Preprocessing in KNIME  
Key preprocessing steps included:  
- **Handling Missing Values:** Median imputation for numerical features; mode imputation for categorical features  
- **Encoding Categorical Variables:** One-hot encoding for company size, label encoding for education levels  
- **Feature Scaling:** Min-max normalization for numerical attributes (e.g., experience, training hours)  
- **Feature Selection:** Recursive Feature Elimination (RFE) to remove low-impact variables  
- **Train-Test Split:** 80% training, 20% testing for unbiased model evaluation  

## 4. Machine Learning Models & Results  
This project implemented and compared multiple classification models:  

| Model                  | Accuracy | Precision | Recall | F1-Score | Cohen’s Kappa |
|------------------------|----------|------------|---------|------------|---------------|
| Random Forest         | 92.5%    | 90.9%      | 88.6%   | 89.7%      | 79.3%         |
| Decision Tree         | 91.6%    | 89.8%      | 87.4%   | 88.5%      | 77.0%         |
| Logistic Regression   | 77.9%    | 70.6%      | 48.05%  | 64.5%      | 30.4%         |
| Gradient Boosted Trees | 81.3%   | 75.4%      | 71.8%   | 73.2%      | 46.6%         |

### Key Takeaways:  
- **Random Forest had the highest accuracy (92.5%)**, making it the best choice for hiring predictions.  
- **Decision Tree performed well but was prone to overfitting.**  
- **Logistic Regression struggled with non-linear relationships, achieving lower accuracy.**  
- **Gradient Boosting performed moderately but was computationally expensive.**  

## 5. Business Impact  
This project demonstrates how machine learning can enhance hiring decisions by:  
- Reducing bias in recruitment through data-driven decision-making  
- Identifying top candidates based on predictive hiring likelihood  
- Streamlining recruitment by focusing on high-probability hires  

## 6. Future Improvements  
- Further hyperparameter tuning to optimize accuracy  
- Incorporating real-time labor market data for better hiring predictions  
- Exploring deep learning approaches (e.g., Neural Networks) for more advanced modeling  
- Comparing results with other ML platforms 

## 7. Repository Contents  
- **`HP_Data_Analysis.knwf`** → KNIME workflow for data preprocessing and model training  
- **`aug_train.csv`** → Training dataset used for model development  
- **`aug_test.csv`** → Testing dataset for model evaluation  
- **`project_report.pdf`** → Full project report detailing methodology and results  
- **`README.md`** → Project documentation  

## 8. How to Use This Repository  
1. **Download the dataset** (if applicable).  
2. **Open KNIME** and import `workflow.knwf`.  
3. **Run the workflow** to reproduce the analysis.  
4. Modify or expand the analysis as needed.  

## 9. Contact  
For any questions or collaboration opportunities, feel free to reach out:  
- **LinkedIn:** www.linkedin.com/in/selena-cha  
- **GitHub:** https://github.com/Selena1224
