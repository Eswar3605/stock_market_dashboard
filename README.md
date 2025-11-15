# 📊 Stock Market ETL + Streamlit Dashboard

This project demonstrates a full **ETL (Extract, Transform, Load) pipeline** for stock market data, along with an interactive **Streamlit dashboard** to explore the cleaned data and aggregations.

---

##  Project Structure

Stock_Assignment/
│── data/ # Raw CSV files
│ └── stock_market.csv
│
│── cleaned/ # Cleaned and aggregated Parquet files
│ ├── cleaned.parquet
│ ├── agg1.parquet
│ └── agg2.parquet
│
│── app.py # Streamlit dashboard
│── process_data.py # Data cleaning and aggregation script
│── aggregations.py # Optional separate aggregation script
│── requirements.txt # Python dependencies
│── README.md
│── screenshots/ # Screenshots for submission


## ⚡ Features

1. **Data Cleaning**
   - Standardizes column names (`snake_case`)
   - Converts dates to `YYYY-MM-DD`
   - Trims whitespace and fixes text case
   - Maps missing values to `pd.NA`
   - Removes duplicate rows

2. **Aggregations**
   - Daily average close price by ticker
   - Average volume by sector
   - Daily returns per ticker

3. **Streamlit Dashboard**
   - Filter by ticker and date range
   - View daily close price and volume charts
   - See aggregation tables for analysis

-

## 🛠 Setup Instructions

1. Clone the repository

bash
git clone https://github.com/<your-username>/Stock-Data-Dashboard.git
cd Stock-Data-Dashboard

2. Create a virtual environment
bash
python -m venv .venv

3. Activate the virtual environment
Windows PowerShell:

Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\.venv\Scripts\activate
Or Command Prompt:

cmd .\.venv\Scripts\activate.bat

Mac/Linux:
bash
source .venv/bin/activate

4. Install dependencies
bash
pip install -r requirements.txt

5. Run data cleaning and generate cleaned.parquet
bash
python process_data.py
This will generate:

cleaned/cleaned.parquet

cleaned/agg1.parquet

cleaned/agg2.parquet


6. Run the Streamlit dashboard
bash
python -m streamlit run app.py
Open the URL in your browser (usually http://localhost:8501).



Main dashboard view

Filtered view by ticker/date

Aggregation tables and charts

⚙ Notes
If parquet files are large, you can exclude them from GitHub and regenerate locally using process_data.py.

Make sure your CSV file (stock_market.csv) is placed in the data/ folder.

Python 3.9+ is recommended.

