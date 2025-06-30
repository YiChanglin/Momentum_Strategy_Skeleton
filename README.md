# Momentum_Strategy_Skeleton

**Simple IBKR Dynamic Momentum Strategy**
This Python algorithm implements a simple dynamic momentum trading strategy for stocks via the Interactive Brokers (IBKR) API. It dynamically adjusts long/short exposure based on market regimes and uses an ATR-based trailing stop-loss for risk management.

**Features**
1. Dynamic Momentum: Trades stocks based on their momentum.
2. Market Regime Adaptation: Adjusts position weighting (long/short) based on SPY's 50-day and 200-day Simple Moving Averages (SMAs).
3. ATR Trailing Stop-Loss: Implements Average True Range (ATR) based trailing stop-loss for open positions.
4. Automated Rebalancing: Periodically rebalances the portfolio.
5. IBKR Integration: Connects to IBKR TWS/Gateway for live trading and data.

**Strategy Overview**
1. Market Regime: SPY SMA 50 vs. SMA 200 determines bullish (more long) or bearish (more short) bias.
2. Momentum Calculation: Volatility-adjusted momentum score calculated for a predefined list of stocks over a lookback period.
3. Position Adjustment: Based on market regime and momentum rank, allocates capital equally to selected long/short positions using market orders.
4. Risk Management: ATR-based trailing stop-loss liquidates positions if triggered.
