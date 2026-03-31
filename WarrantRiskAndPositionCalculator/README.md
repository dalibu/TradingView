# Universal Warrant Position Sizer Pro (Pine Script v6)

A professional-grade risk and position management tool for TradingView, suitable for all asset classes (stocks, indices, commodities, forex) and especially for leveraged derivatives such as warrants/options.

## Key Features

- **Long & Short Support:** Calculates position sizes for Calls (Long) and Puts (Short).
- **Asset-agnostic:** Works on any chart, as all calculations are percentage-based.
- **Precise Position Sizing:** Exact quantity based on a fixed risk budget (e.g., $100 or €100).
- **Fee & Spread Awareness:** Transaction costs (buy/sell) and spread are realistically included.
- **Flexible Stop-Loss Modes:**
    - **Manual:** Fixed SL price and entry price.
    - **ATR-based:** Automatic SL calculation based on volatility (ATR).
- **Dynamic Dashboard:** Clear table with all key figures, freely placeable and with adjustable font size.
- **Visualization:** SL and all TP levels are shown as labeled lines on the chart. In ATR mode, the SL path is plotted as a line.
- **Fee-adjusted Take-Profit:** TP levels are calculated so that the desired risk/reward ratio is achieved after all costs.

## Usage

1. **Add Script:** Copy the Pine Script into the TradingView editor and add it to your chart.
2. **Open Settings:**
     - **Trade Direction:** Choose Long (Call) or Short (Put).
     - **Warrant Data:** Enter current Ask price, leverage, and spread.
     - **Risk Settings:** Set your maximum risk amount and per-order fees.
     - **Stop-Loss Settings:**
         - **Manual:** Enter entry price and SL price of the underlying asset.
         - **ATR-Based:** Choose ATR length and multiplier; SL is calculated automatically.
     - **User Interface:** Choose dashboard position and font size.
3. **Read Results:**
     - Optimal quantity, SL price, all TP levels (including net profit), and the corresponding asset prices are displayed.
     - SL and TP lines appear directly on the chart.

## Calculation Logic

- **Risk Budget:** Net risk after deducting all fees.
- **Position Size:** Quantity so that the maximum loss (including fees & spread) does not exceed the budget.
- **TP Levels:** Calculated so that, after fees, the desired RRR (e.g., 2:1) is achieved net.
- **ATR Mode:** SL follows volatility and is shown as a line.

---
*Disclaimer: Trading leveraged derivatives involves significant risk of capital loss. This script is intended for calculation and educational purposes only.*
