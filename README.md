# options-backtesting
Testing options strategy using Black Scholes model

- Project name: synthetic Black-Scholes backtest
- Strategy name: Short iron butterfly

# Agenda of the project
academically useful for demonstrating strategy mechanics, but you should explicitly state that it is not a substitute for real market data validation.

# Observations
- The strategy is outperforming for stocks with stationary prices

# Assumptions
- Margin calculated is 3 times of premium received in case of option selling
- Black-Scholes assumes constant volatility and log-normal returns, which rarely hold in reality.

# Limitations
- You're using realized volatility to price options, whereas real market prices reflect implied volatility (which includes volatility risk premium and changes dynamically).
- You will miss volatility smile/skew, term structure, liquidity issues, wide bid-ask spreads (common in Indian options), and execution slippage.
- Result: The backtest will likely overstate profitability and not reflect real-world P&L.

# Precautions
This should be treated only as a preliminary/theoretical analysis. It is not reliable enough for live deployment decisions. Many strategies look good in synthetic backtests but fail in live trading due to the factors above.