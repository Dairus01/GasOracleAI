# Ethereum Gas Price Tracker and Predictor

## Overview
This script fetches Ethereum gas prices from the Etherscan API, stores the data for three hours, analyzes trends, and predicts the lowest gas price in the next 10 minutes using polynomial regression. The results are visualized with an interactive graph using Plotly.

## Features
- **Real-time Gas Price Retrieval**: Fetches gas prices from the Etherscan API every 0.5 seconds.
- **Data Storage**: Stores gas price data over a 3-hour period.
- **Trend Analysis**: Identifies the lowest gas price within the collected timeframe.
- **Prediction Model**: Uses polynomial regression to predict the next 10 minutes of gas prices.
- **Data Visualization**: Displays a graph of historical and predicted gas prices using Plotly.
- **CSV Export**: Saves collected data to `gasprices.csv` for further analysis.

## Requirements
Ensure you have the following dependencies installed before running the script:

```bash
pip install requests pandas plotly numpy scikit-learn
```

## How to Use
1. **Set Up Your API Key**:
   - Replace `"Please input your API key"` in the script with your valid Etherscan API key.

2. **Run the Script**:
   - Execute the script in a Python environment.

   ```bash
   python script.py
   ```

3. **Data Collection & Analysis**:
   - The script will run for **3 hours**, collecting gas prices every 0.5 seconds.
   - It prints the lowest gas price in the last 3 hours and predicts the lowest gas price in the next 10 minutes.

4. **Visualization**:
   - An interactive graph is generated, displaying historical, predicted, and rolling average gas prices.

5. **CSV Export**:
   - The collected gas price data is saved as `gasprices.csv`.

## Example Output
```
Lowest gas price in the last 3 hours: 15 Gwei at 2024-03-19 14:32:10
Expected lowest gas price in next 10 minutes: 14.35 Gwei at 2024-03-19 14:41:55
Gas price data saved to gasprices.csv
```

## Customization
- **Change Data Collection Duration**: Modify `10800` (seconds) in the while-loop condition to adjust how long data is collected.
- **Modify Prediction Window**: Adjust the `120` points in `predict_timestamps` for a longer or shorter prediction timeframe.
- **Visualization Enhancements**: Modify `plotly.graph_objects` parameters to customize the appearance of the graph.

## Notes
- If the API request fails, the script will retry up to 3 times before skipping the data point.

## License
This project is released under the MIT License.

---

Happy tracking! 🚀

## This code is written by Okoh Dairus 