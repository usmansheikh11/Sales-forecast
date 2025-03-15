# Store Sales Time Series Forecasting

## Kaggle Project: Sales Forecasting for the Next 15 Days

### Overview
This project aims to forecast store sales for the next 15 days using various time series models, including:
- **ARIMA** (AutoRegressive Integrated Moving Average)
- **SARIMA** (Seasonal ARIMA)
- **Prophet** (Facebook's time series forecasting model)
- **Ensemble Model** (Averaging predictions from the above models)

### Datasets Used
The following datasets are utilized in this project:
- **train.csv**: Historical sales data
- **test.csv**: Test dataset for which predictions need to be made
- **stores.csv**: Metadata about stores (e.g., store type)
- **oil.csv**: Daily oil prices
- **holidays_events.csv**: Holiday and event calendar
- **sample_submission.csv**: Example submission format

### Project Workflow
1. **Data Loading & Preprocessing**
   - Convert date columns to datetime format
   - Handle missing values (especially in oil prices)
   - Feature engineering (e.g., extracting year, month, day, holidays, etc.)
2. **Exploratory Data Analysis (EDA)**
   - Sales trends over time
   - Sales distribution by store type and product family
   - Impact of holidays and oil prices on sales
3. **Time Series Modeling & Forecasting**
   - **ARIMA Model**: Univariate forecasting
   - **SARIMA Model**: Seasonal forecasting with external regressors
   - **Prophet Model**: Incorporating trends, seasonality, holidays, and regressors
   - **Ensemble Forecasting**: Combining multiple models for better accuracy
4. **Submission Preparation**
   - Distribute total forecasted sales across store-product combinations
   - Generate the final submission file (`sales_forecast_submission.csv`)

### Visualizations
Several interactive visualizations are generated using **Matplotlib**, **Plotly**, and **Seaborn**, including:
- Total sales over time
- Sales by store type
- Sales correlation with oil prices
- Sales distribution on holidays vs regular days
- Time series decomposition (trend, seasonality, residuals)
- Model performance comparisons

### Technologies Used
- **Python**
- **Pandas, NumPy** (Data Manipulation)
- **Matplotlib, Seaborn, Plotly** (Data Visualization)
- **Statsmodels** (ARIMA, SARIMA models)
- **Prophet** (Forecasting model)
- **Scikit-learn** (Metrics and model evaluation)

### Installation & Usage
#### Prerequisites
Ensure you have Python installed along with the necessary libraries. You can install dependencies using:
```bash
pip install pandas numpy matplotlib plotly seaborn statsmodels prophet scikit-learn tqdm
```

#### Running the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/sales-forecasting.git
   cd sales-forecasting
   ```
2. Place the dataset files (`train.csv`, `test.csv`, `stores.csv`, `oil.csv`, `holidays_events.csv`) in the project directory.
3. Run the script:
   ```bash
   python sales_forecasting.py
   ```
4. The forecast results will be saved in `sales_forecast_submission.csv`.

### Results & Forecasting Performance
- The models generate a **15-day sales forecast** for each store-product combination.
- Performance is evaluated using **Mean Squared Error (MSE)** and **Mean Absolute Error (MAE)**.
- **Ensemble Model** provides the best overall accuracy by combining ARIMA, SARIMA, and Prophet predictions.

### Future Improvements
- Hyperparameter tuning for improved accuracy
- Incorporation of additional external factors (e.g., weather data)
- Deep learning-based models for enhanced performance


