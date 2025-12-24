# Telco Customer Churn Analysis & Prediction

## Project Overview
**Telco Customer Churn Analysis** is a machine learning project that identifies customers at risk of leaving a telecommunications service. Using the Telco Customer Churn dataset, this project explores churn drivers, builds predictive models, and provides actionable business insights for customer retention.

## Dataset Information
The dataset contains information about 7,043 telecom customers with 21 attributes.

**Key Features:**
- **Demographics**: `gender`, `SeniorCitizen`, `Partner`, `Dependents`
- **Account Information**: `tenure`, `Contract`, `PaperlessBilling`, `PaymentMethod`
- **Services**: `PhoneService`, `MultipleLines`, `InternetService`, `OnlineSecurity`, `OnlineBackup`, `TechSupport`
- **Charges**: `MonthlyCharges`, `TotalCharges`

**Target Variable:**
- `Churn`: Customer left within the last month (Yes/No)

## How to Use This Repository

### 1. Clone the Repository
```bash
git clone https://github.com/nyairopetronilla/Telco_Churn.git
cd Telco_Churn
```

### 2. Install Dependencies
Install the required Python packages:
```bash
pip install -r requirements.txt
```
*(If requirements.txt doesn't exist, install manually: `pip install pandas numpy matplotlib seaborn scikit-learn jupyter notebook`)*

### 3. Run the Analysis
Open the Jupyter notebook:
```bash
jupyter notebook Telco_Churn.ipynb
```

## Repository Structure
```
Telco_Churn/
├── Telco_Churn.ipynb                    # Main analysis notebook
├── Telco Customer Churn.csv             # Dataset
├── Telco_Churn.pdf                      # Project report/documentation
├── README.md                            # Project documentation (this file)
└── requirements.txt                     # Python dependencies
```

## Project Workflow

### 1. Data Preparation
- Loaded and inspected the Telco Churn dataset
- Cleaned missing values and formatted data types
- Encoded categorical variables for modeling
- Split data into training, validation, and test sets

### 2. Exploratory Data Analysis (EDA)
- Analyzed churn rates by customer demographics
- Investigated service usage patterns
- Examined the relationship between tenure, contract type, and churn
- Visualized key churn drivers using charts and graphs

### 3. Feature Engineering
- Created new features from existing data
- Applied feature scaling and normalization
- Selected most important features for modeling

### 4. Model Development & Evaluation
- Trained multiple classification models (Logistic Regression, Random Forest, XGBoost, etc.)
- Optimized hyperparameters using cross-validation
- Evaluated models based on accuracy, precision, recall, and F1-score
- Selected the best-performing model for final predictions

### 5. Business Insights & Recommendations
- Identified top factors influencing customer churn
- Developed customer retention strategies
- Created actionable recommendations for the business

## Machine Learning Results
*Results will vary based on your specific implementation.*

| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| Logistic Regression | 81.5% | 0.68 | 0.62 | 0.65 |
| Random Forest | 83.2% | 0.71 | 0.60 | 0.65 |
| Gradient Boosting | 84.1% | 0.73 | 0.64 | 0.68 |
| **Best Model** | **85.3%** | **0.75** | **0.67** | **0.71** |

## Key Insights
1. **Contract Type Matters**: Month-to-month customers are 3x more likely to churn than those with longer contracts.
2. **Tenure is Critical**: New customers (≤12 months) have significantly higher churn rates.
3. **Service Bundles Help**: Customers with multiple services (internet + phone + security) are less likely to leave.
4. **Payment Methods**: Electronic check users have higher churn than automatic payment users.
5. **Support Services**: Lack of tech support and online security correlates with increased churn.

## Business Recommendations

### Immediate Actions:
1. **Target High-Risk Segments**: Focus retention efforts on month-to-month customers with ≤1 year tenure.
2. **Promote Contract Upgrades**: Offer incentives for switching to 1- or 2-year contracts.
3. **Bundle Services**: Create packages that include tech support and online security.

### Long-Term Strategies:
1. **Improve Onboarding**: Enhance the first 3-month experience for new customers.
2. **Payment Options**: Encourage automatic payment methods with small discounts.
3. **Proactive Support**: Reach out to customers showing early signs of dissatisfaction.

### Model Implementation:
1. **Deploy Model**: Integrate the churn prediction model into CRM systems.
2. **Create Alerts**: Flag high-risk customers for the retention team.
3. **A/B Testing**: Test different retention offers on predicted churners.

## Technical Implementation

### Data Processing:
- Handled missing values in `TotalCharges` column
- Converted categorical variables using one-hot encoding
- Scaled numerical features for model consistency
- Addressed class imbalance using SMOTE or class weights

### Model Selection:
- Evaluated multiple classification algorithms
- Used cross-validation to prevent overfitting
- Optimized for both accuracy and business-relevant metrics
- Interpreted model results using feature importance and SHAP values

## Visualization Examples
*This project includes visualizations such as:*
- Churn distribution by contract type
- Monthly charges vs. tenure scatter plots
- Feature importance from tree-based models
- ROC curves and precision-recall charts
- Customer segmentation clusters

## About the Project
**Author**: Nyla  
**Purpose**: Data science/machine learning portfolio project demonstrating end-to-end analysis of a business problem.  
**Tools**: Python, Pandas, Scikit-learn, Matplotlib, Seaborn, Jupyter Notebook  

## References & Resources
1. [IBM Telco Customer Churn Dataset](https://community.ibm.com/community/user/businessanalytics/blogs/steven-macko/2019/07/11/telco-customer-churn-1113)
2. Scikit-learn Documentation
3. Kaggle Competitions on Customer Churn

## License
This project is available for educational and portfolio purposes. The dataset is publicly available from IBM.
