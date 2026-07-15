# Alpaca Bot Vercel Dashboard

This folder is ready to deploy as a static Vercel site.

Files:
- `index.html` - dashboard UI
- `metrics_history.json` - all EOD metric days in one file
- `vercel.json` - small static-site config

Deploy steps:
1. Push this `vercel_dashboard` folder to a GitHub repo.
2. In Vercel, click Add New Project.
3. Import the repo.
4. Set the project root to this folder if needed.
5. Framework preset: Other / static.
6. Deploy and share the Vercel URL with your group.

To refresh the dashboard after each EOD report, regenerate `metrics_history.json` from the JSON files in `../metrics_history` and push the updated file.

## Filters

The dashboard filters by Alpaca account, crypto/trading symbol, and trading day.
The symbol selector is populated from each account dataset's `by_symbol` keys;
the bot's internal `BTCUSDT` feed identifier is displayed as the executed
Alpaca pair `BTC/USD`, and all cards, charts, positions, and trade logs are
recalculated for the selected symbol.

