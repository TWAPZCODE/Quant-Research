# QUANT RESEARCH 

A collection of systematic trading resreach covering alpha signal discovery, trend-following strategies, and volatility regime analysis. Each study follows a hypothesis-driven workflow.

# Research Modules

1. ALPHA RESEARCH NOTEBOOK
   Exploratory factor research testing on alpha signals.
   - Signal construction  and normalization (z-scoring,ranking).
   - Information Coefficient (IC) analysis and signal decay curves.
   - Quantile portfolio returns an long-short spread analysis.
   - Turnover an transaction cost consideration.
   KEY QUESTION: Does the signal have predictive power? How fast does it decay? Does it survive costs?

2. MOVING AVERAGE TREND FOLLOWING NOTEBOOK (eventually going to be extended to fullfil ML capabilities)
   Systematic study of Moving Average-based trend strategies across lookback windows.
   - Single and multi moving average crossover systems.
   - Parameter sensitivity analysis (avoiding overfit lookbacks).
   - In-sample vs out-of-sample comparison.
   KEY QUESTIONS: Is trend persistence statistically significant? Which parameterizations are robust rather than curve-fit?

3. VOLATILITY REGIME CLASSIFICATION NOTEBOOK
   Classifying market states by volatility to condition strategy behviour.
   - Realized volatility estimation across horizons.
   - Regime detection and classification of high/low volatility states.
   - Regime transition analysis and persistence statistics.
   - Strategy performance conditioned on regime.
   KEY QUESTIONS: Are regimes persistent enough to trade on? Does trend-following performance differ across volatility states?

 # METHODOLOGY NOTES
 - All results reported gross and net of assumed transaction costs.
 - Out-of-sample periods held out from parameter selection.
 - No survivorship-bias-free guarantees on free data sources - noted where relevant.

 # TECH STACK
 Python * pandas * NumPy * matplotlib * statsmodels * scikit-learn * Jupyter

 # Roadmap
 - Extend alpha research with multi-factor combination.
 - Add regime-conditioned position sizing to trend strategy.
 - Build event-driven backtester for realistic execution modeling.

 # DISCLAIMER
 This repository is for research and educational purposes only and does not constitute investment advice.


 
MIT (or your preferred license)
