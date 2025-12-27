# Manufacturing Defect Cost Prediction

This project uses Python to study 1,000 defect records from a factory and try to predict which defects will have a high repair cost.

## Data

Each row in the CSV file has:
- product_id
- defect_type
- defect_location
- severity
- inspection_method
- defect_date
- repair_cost

From repair_cost we create a new column:
- high_cost (1 = expensive defect, 0 = cheaper defect)

## What I did

1. Cleaned the data:
   - Converted defect_date to real date.
   - Created year, month, and day_of_week columns.
   - Removed extra spaces in text columns.

2. Explored the data:
   - Plotted number of defects by type and location.
   - Plotted repair cost by severity.

3. Built a model:
   - Used one-hot encoding for categorical columns.
   - Trained a Random Forest classifier to predict high_cost.
   - Tried class weights to handle imbalanced data.
   - Checked performance with confusion matrix, precision, and recall.

4. Looked at feature importance:
   - Found which columns (product, defect type, location, etc.) are most related to high repair cost.

## Tools

Python, pandas, numpy, scikit-learn, matplotlib, seaborn, Google Colab.
