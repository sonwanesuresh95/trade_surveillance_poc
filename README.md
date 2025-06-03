# 🛡️ Trade Surveillance System (PoC)

This is a **Proof of Concept (PoC)** for a Trade Surveillance System implemented using Python and Jupyter Notebook.  
It analyzes trading behavior to detect potential **spoofing** activities based on order patterns.

## 📁 Project Structure

```
.
├── trade_surveillance_poc.ipynb   # Jupyter Notebook with code and logic
├── trade_data.csv                 # Sample trade/order data
└── README.md                      # Project documentation
```

## 📊 Functionality

- Loads trade and order data from a CSV file.
- Detects **spoofing behavior** based on a high cancel-to-order ratio.
- Generates alerts for suspicious traders.
- Uses simple, explainable rule-based logic for analysis.

## 📂 Sample Data Format (`trade_data.csv`)

| timestamp           | order_id | trader_id | symbol | side | price | quantity | status   |
|---------------------|----------|-----------|--------|------|-------|----------|----------|
| 2024-06-03 10:00:00 | 1        | TR123     | AAPL   | buy  | 185.0 | 100      | placed   |
| 2024-06-03 10:00:01 | 2        | TR123     | AAPL   | buy  | 185.0 | 100      | canceled |
| ...                 | ...      | ...       | ...    | ...  | ...   | ...      | ...      |

## ⚙️ Requirements

Install dependencies:

```bash
pip install pandas
```

## 🚀 How to Use

Open and run the notebook:

```bash
jupyter notebook trade_surveillance_poc.ipynb
```

The notebook:
- Loads the CSV data
- Applies spoofing detection rules
- Prints alerts for suspicious activity

## 📌 Spoofing Detection Logic

A trader is flagged if:
- Total orders >= 5
- Cancel-to-order ratio > 0.4

## 📈 Future Enhancements

- Real-time data ingestion using Kafka/WebSockets
- More rules (e.g., wash trades, front-running)
- Database integration for alert logging
- Streamlit dashboard for visualization
- Dockerized deployment

## 🧠 Author

Built by a python engineer exploring trade surveillance systems using Python.

## 📄 License

This project is open-source and free to use under the MIT License.
