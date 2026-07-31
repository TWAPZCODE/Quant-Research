# Moving Average Trend-Following Backtester

This project tests a simple trading strategy to see if it would have made money in the past — and compares it to just buying and holding.

## What does it do?

It downloads historical daily price data (default: **NQ=F**, the Nasdaq-100 futures) and follows one simple rule:

- If the price is **above** its recent average → go **long** (bet the price goes up)
- If the price is **below** its recent average → go **short** (bet the price goes down)

This is called a "moving average" strategy — it tries to ride trends instead of guessing tops and bottoms.

The notebook then compares two outcomes over the same time period:
1. **Buy and hold** — just buy at the start and never touch it (the benchmark)
2. **The strategy** — following the moving average rule the whole way through

It shows both as a chart so you can see which one performed better, plus numbers for yearly return and the worst drop from a peak (drawdown).

## What you'll need

```
python >= 3.9
yfinance
pandas
numpy
matplotlib
```

Install everything with:
```bash
pip install yfinance pandas numpy matplotlib
```

## How to use it

1. Open the notebook in Jupyter.
2. Change the settings at the top if you want:
   - How much starting money (`starting_balance`)
   - How many days the moving average looks back (`ma`)
   - Which asset, time frame, and date range to test (`ticker`, `interval`, `start`, `end`)
3. Run all the cells from top to bottom.

## How it actually works (a bit more detail)

- Daily gains/losses are calculated day by day.
- The strategy only acts on **yesterday's** signal, not today's — this avoids "cheating" by using information you wouldn't have had in real time.
- Money grows or shrinks by compounding these daily returns, starting from your chosen balance.

## Important limitations — please read

This is a learning/research project, **not financial advice**, and it's simplified on purpose:
- It doesn't include trading fees, spreads, or slippage — real trading costs money every time you buy or sell.
- It assumes you can always go short and long freely, with no extra cost or margin requirements.
- It only tests one setting (a 20-day average) — it hasn't been checked across different settings to see if it still works.
- Just because it performed well (or badly) in the past doesn't mean it will do the same in the future.

## License

MIT (or your preferred license)
