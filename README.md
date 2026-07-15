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

The primary data-source dropdown includes Alpaca Live, Alpaca Paper, and Alpaca
Crypto. Crypto metrics use the `alpaca_crypto` dataset and the executed Alpaca
pair is `BTC/USD`.
The crypto strategy uses one take-profit at 1.5R and closes 100% at that target.
Crypto metrics are loaded from `crypto_metrics_history.json` so the independent
equities metrics automation cannot overwrite them.

