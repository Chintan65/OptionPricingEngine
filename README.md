# Option Pricing & Backtesting Engine

## **Overview**

A high-performance **Option Pricing Engine** developed in **C++** to value derivatives and simulate dynamic delta-hedging strategies. The system implements both analytical and numerical methods to price European options and provides a robust backtesting framework to analyze hedging errors across diverse market scenarios.
* **Multi-Model Pricing Engine** : Implements **Black-Scholes** (analytical), **Binomial Tree** (iterative/Cox-Ross-Rubinstein), and **Monte Carlo** (stochastic simulation) models.
* 
```plaintext
OptionPricingEngine/
├── src/            # C++ Source (Engine, Backtester, Logger)
├── include/        # C++ Headers (Pricing Interface, Types)
├── scripts/        # Python Tools (Data retrieval, Metrics, Plotting)
├── data/           # Market datasets (CSV)
├── logs/           # Backtest results and system logs
└── Makefile        # Build automation
```

Performance

![1771322520834](image/README/1771322520834.png)

How to Run

```bash
# 1. Generate/Fetch Data (Yahoo Finance, Synthetic, and Bloomberg formats)
python3 scripts/data_manager.py
# 2. Compile the C++ Engine (Optimized with -O3 and -pthread)
make clean && make
# 3. Run the Backtest Simulation
./OptionEngine
# 4. View raw results
ls -l logs/
# 5. Visualize Hedging Error
python3 scripts/plot_results.py
# 6. Calculate Quantitative Risk Metrics
python3 scripts/final_metrics.py
```
