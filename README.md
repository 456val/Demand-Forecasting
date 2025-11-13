# Predictive Analytics for Inventory Management

This project applies machine learning techniques to improve inventory management through accurate demand forecasting. It uses historical sales data to predict which products are likely to run out and suggests optimal restock quantities.

## Project Overview

The notebook focuses on predicting future product demand to prevent stockouts and overstocking. It uses a dataset containing:
- Product line and category
- Order status and deal size
- Order date and quantity ordered
- Customer information and territory

The model helps businesses optimize stock levels, improve supply chain decisions, and anticipate seasonal demand patterns.

## Objectives

The goal is to build a data-driven forecasting system that:
1. Identifies products likely to sell out in the upcoming month
2. Suggests ideal restock amounts
3. Provides insights into product performance by line and region

## Technologies Used

- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Data Preprocessing

Steps include:
- Checking and handling missing values
- Replacing missing customer names with "Anonymous"
- Filling unknown addresses with "Unknown"
- Handling missing phone numbers by substituting with "0"
- Encoding categorical variables and cleaning inconsistent text

Example:
```python
df['CUSTOMERNAME'] = df['CUSTOMERNAME'].fillna("Anonymous")
df['ADDRESS'] = df['ADDRESS'].fillna("Unknown")
df['PHONE'] = df['PHONE'].fillna('0')

## Model Development

Machine learning algorithms are used to model the relationship between:

- Historical demand (quantity ordered)
- Product line and deal size
- Order date and region

These relationships are used to forecast future demand for each product.

## Key Outputs

- Forecasted demand for upcoming months
- Identification of high-risk products (likely to stock out)
- Insights into top-performing product lines
- Data visualization of historical vs. predicted demand

### Example Output

| Product Line | Month       | Predicted Demand | Restock Suggestion |
|---------------|-------------|------------------|--------------------|
| Classic Cars  | March 2024  | 540              | +60 units          |
| Motorcycles   | March 2024  | 210              | +25 units          |

## Future Improvements

- Integrate Prophet or LSTM models for advanced time-series forecasting
- Automate retraining of the model with new monthly data
- Add alert notifications for products nearing low stock thresholds
- Develop an interactive dashboard using Streamlit or Power BI
- Connect to an SQL or cloud database for real-time demand tracking

## Use Cases

- Inventory management and stock optimization
- Predictive analytics for supply chain decisions
- Sales and demand pattern analysis
- Business forecasting and production planning
- Reducing costs from overstocking or understocking

## License

This project is licensed for educational and research purposes only.  
It may be used, modified, and shared for non-commercial applications.  
Please ensure that all data used complies with privacy, confidentiality, and ethical use standards.




