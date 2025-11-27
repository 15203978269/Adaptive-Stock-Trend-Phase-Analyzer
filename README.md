# Adaptive Stock Trend Phase Analyzer

An intelligent Python tool that automatically detects and classifies trend phases in stock prices with adaptive parameter tuning.

## 🚀 Features

- **Adaptive Parameter Tuning**: Automatically adjusts sensitivity based on desired phase count
- **Multi-criteria Trend Detection**: Combines slope analysis and price change percentages
- **Smart Phase Merging**: Intelligently consolidates phases using duration, trend compatibility, and price proximity
- **Flexible Output**: Generate 5-15+ phases based on analysis needs
- **yFinance Integration**: Easy stock data retrieval

## 📊 How It Works

1. **Data Collection**: Fetches monthly historical data using yfinance
2. **Trend Calculation**: Uses rolling linear regression to calculate price slopes
3. **Phase Identification**: Groups consecutive months with similar trends
4. **Adaptive Consolidation**: Merges phases to reach target count using smart scoring
5. **Classification**: Categorizes as Strong_Uptrend, Uptrend, Downtrend, Strong_Downtrend, or Consolidation

## 🛠 Usage

```python
# Simple one-parameter control
result, phases_df = analyze_stock_phases("NAME OF STOCK", target_phases=8)
