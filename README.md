# Production Defect Cost Prediction and Analysis

## Project Overview
This project analyzes manufacturing defect data to identify factors associated with high repair costs. The goal is to provide insights for quality monitoring and defect prevention by predicting defects likely to incur high costs.

## Dataset
- 1,000 historical defect records
- Features include defect type, defect location, severity, inspection method, product ID, defect date, and repair cost
- Data contains both categorical and numerical variables

## Methodology
1. **Data Cleaning and Preprocessing**
   - Converted defect date to datetime
   - Created time-based features: month, day of week
   - Cleaned categorical columns
2. **Feature Engineering**
   - Selected relevant features
   - One-hot encoded categorical variables
3. **Exploratory Data Analysis (EDA)**
   - Plotted defects by type, location, and repair cost by severity
4. **Target Definition**
   - Defined high-cost defects as the top 25% of repair costs
5. **Train-Test Split**
   - Stratified 80/20 split to handle class imbalance
6. **Random Forest Modeling**
   - Baseline classifier with class_weight='balanced'
   - Evaluated with confusion matrix and precision/recall metrics
7. **Feature Importance Analysis**
   - Identified key contributors to high repair costs

## Key Findings
- Repair costs are strongly influenced by:
  - Product-specific factors
  - Defect severity
  - Defect type
  - Defect location
  - Inspection method
- High-cost defects are relatively rare (25%), resulting in class imbalance
- Baseline Random Forest model achieved reasonable overall accuracy, but recall for high-cost defects was low, highlighting the need for additional data or advanced imbalance handling techniques

## Tools & Technologies
- Python
- pandas
- scikit-learn
- Matplotlib
- Seaborn
- Google Colab

## Future Improvements
- Apply SMOTE or other resampling techniques for class imbalance
- Implement cost-sensitive learning
- Introduce domain-specific cost thresholds
- Experiment with alternative models such as XGBoost or Logistic Regression

## Author
Nishadi  Ananda  
BSc Statistics (Honours) – 3rd Year
