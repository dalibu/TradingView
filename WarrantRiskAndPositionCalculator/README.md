# Universal Warrant Position Sizer & Risk Manager (Pine Script v6)

A professional-grade risk management tool for TradingView designed for traders using **leveraged warrants (Optionsscheine)** or other delta-1 derivatives. This script works across all asset classes, including stocks, indices, commodities, and forex.

## Key Features

*   **Directional Flexibility:** Supports both **Long (Calls)** and **Short (Puts)** trade directions.
*   **Asset Agnostic:** Works on any chart (Gold, DAX, Apple, BTC, etc.) by calculating percentage-based price movements.
*   **Precision Position Sizing:** Calculates the exact number of units to buy based on a fixed monetary risk budget (e.g., $100 or €100).
*   **Cost & Spread Awareness:** Factors in transaction fees (buy/sell) and the bid-ask spread to ensure your real-world loss stays within your budget.
*   **Derivative SL & TP Mapping:** 
    *   Translates your technical chart Stop-Loss into the corresponding warrant price.
    *   Projects Take-Profit targets for both the warrant and the underlying asset based on Risk/Reward Ratios (1:1, 2:1, 3:1).

## How to Use

1.  **Script Setup:** Copy the Pine Script code into the TradingView Pine Editor and add it to your chart.
2.  **Input Data:** Open the script settings (gear icon):
    *   **Trade Direction:** Select "Long" for Call warrants or "Short" for Put warrants.
    *   **Warrant Data:** Enter the current Ask price, the Leverage (e.g., 15x), and the current Spread.
    *   **Risk Settings:** Define your max risk budget and per-order fees.
    *   **Technical SL:** Enter the price level of the underlying asset where you want to exit the trade.
3.  **Execution:** The dashboard on the top-right will display:
    *   **Optimal Quantity:** The exact number of warrants to purchase.
    *   **Warrant SL:** The price at which you should set your Stop-Loss order at your broker.
    *   **Asset Targets:** The price levels the underlying asset needs to reach to hit your TP goals.

## Calculation Logic

The script follows a rigorous mathematical approach:
1.  **Relative Distance:** Measures the % distance between the current asset price and the Stop-Loss.
2.  **Leverage Multiplier:** Multiplies the asset's % move by the warrant's leverage to determine the warrant's price sensitivity.
3.  **Net Budgeting:** Subtracts total transaction fees from the risk budget before calculating units.
4.  **Spread Compensation:** Deducts the spread from the calculated Stop-Loss price to provide a realistic "Bid" exit price.

---
*Disclaimer: Trading leveraged derivatives involves significant risk of capital loss. This script is intended for calculation and educational purposes only.*
