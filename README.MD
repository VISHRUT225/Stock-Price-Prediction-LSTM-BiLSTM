# Stock Price Prediction using LSTM/Bi-LSTM on Yahoo-Finance Data 📈🤖

![](images/lstm-bilstm.jpeg)

[![Python Version](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/)  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## Overview 🚀  
This project applies advanced deep learning models—**LSTM** and **Bidirectional LSTM (Bi-LSTM)**—to forecast stock prices using historical data from Yahoo Finance. By capturing complex temporal patterns in financial data, our approach aims to assist investors and analysts in making data-driven decisions.

## Table of Contents 💑  
- [Overview](#overview-🚀)  
- [Key Features](#key-features-✨)  
- [Methodology](#methodology-🛠️)  
- [Results](#results-📊)  
- [Installation](#installation-💻)  
- [Usage](#usage-🚀)  
- [Future Work](#future-work-🔮)  
- [License](#license-📝)

## Key Features ✨  
- **Advanced Models:** Uses both LSTM and Bi-LSTM for robust time series prediction.  
- **Data Preprocessing:** Handles noisy and high-dimensional financial data with normalization and sequence generation.  
- **Metadata Integration:** Embeds stock ticker and sector information to enhance model performance.  
- **Ensemble Forecasting:** Combines predictions from multiple models for improved accuracy.  
- **Visualization:** Provides clear graphs comparing predicted and actual stock prices.

## Methodology 🛠️  
1. **Data Acquisition & Preparation:**  
   - Download historical 'Close' prices from Yahoo Finance.  
   - Clean and preprocess data: remove missing values, normalize prices, and convert data into sequences.  
   - Encode stock tickers and sectors as categorical variables for embedding.

2. **Model Construction:**  
   - **LSTM Model:** Two-layer LSTM network with dropout to capture sequential trends.  
   - **Bi-LSTM Model:** Bidirectional LSTM network for capturing both forward and backward dependencies.  
   - Merge metadata embeddings with sequence outputs, then use dense layers to predict the next day’s stock price.

3. **Training & Evaluation:**  
   - Split data into training (80%) and testing (20%) sets.  
   - Train models using the Adam optimizer, early stopping, and model checkpointing.  
   - Evaluate performance using metrics like RMSE, MAE, and R², and visualize predictions.

4. **Forecasting & Model Expansion:**  
   - Functions to forecast new stock data and expand the model to include new tickers.  
   - Fine-tune the model for improved performance on new data.

## Results 📊  
- **Performance:** Ensemble predictions show lower error rates than individual LSTM or Bi-LSTM models.  
- **Visualization:** Graphs effectively compare actual vs. predicted prices, highlighting model accuracy.  
- **Insights:** The models capture both short-term fluctuations and long-term trends in stock prices.

## Installation 💻  
1. **Clone the Repository:**  
   ```bash
   git clone https://github.com/VISHRUT225/Stock-Price-Prediction-LSTM-BiLSTM.git
   cd stock-price-prediction
   ```

2. **Create a Virtual Environment (Optional but Recommended):**  
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies:**  
   ```bash
   pip install -r requirements.txt
   ```

## Usage 🚀  
- **Training the Model:**  
  Open the Jupyter Notebook `stock_price_prediction.ipynb` and run all cells to execute data preprocessing, model training, and evaluation.
  
- **Inference:**  
  Use the provided inference functions in the notebook to predict stock prices for a given ticker and date range.

## Future Work 🔮  
- **Model Enhancements:** Explore additional architectures (e.g., Transformer models) for even better performance.  
- **Feature Expansion:** Incorporate more financial indicators and sentiment analysis to further improve predictions.  
- **Deployment:** Develop a real-time forecasting tool for live stock market predictions.

## License 📝  
This project is licensed under the [MIT License](LICENSE).

---

Happy forecasting and investing! 💡📈🤖

