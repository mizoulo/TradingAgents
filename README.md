<p align="center">
  <img src="assets/TauricResearch.png" style="width: 60%; height: auto;">
</p>

<div align="center" style="line-height: 1;">
  <a href="https://arxiv.org/abs/2412.20138" target="_blank"><img alt="arXiv" src="https://img.shields.io/badge/arXiv-2412.20138-B31B1B?logo=arxiv"/></a>
  <a href="https://discord.com/invite/hk9PGKShPK" target="_blank"><img alt="Discord" src="https://img.shields.io/badge/Discord-TradingResearch-7289da?logo=discord&logoColor=white&color=7289da"/></a>
  <a href="./assets/wechat.png" target="_blank"><img alt="WeChat" src="https://img.shields.io/badge/WeChat-TauricResearch-brightgreen?logo=wechat&logoColor=white"/></a>
  <a href="https://x.com/TauricResearch" target="_blank"><img alt="X Follow" src="https://img.shields.io/badge/X-TauricResearch-white?logo=x&logoColor=white"/></a>
  <br>
  <a href="https://github.com/TauricResearch/" target="_blank"><img alt="Community" src="https://img.shields.io/badge/Join_GitHub_Community-TauricResearch-14C290?logo=discourse"/></a>
</div>

<div align="center">
  <!-- Keep these links. Translations will automatically update with the README. -->
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=de">Deutsch</a> | 
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=es">Español</a> | 
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=fr">français</a> | 
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=ja">日本語</a> | 
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=ko">한국어</a> | 
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=pt">Português</a> | 
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=ru">Русский</a> | 
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=zh">中文</a>
</div>

---

# TradingAgents: Multi-Agents LLM Financial Trading Framework

> **Personal fork** — I'm using this for learning and experimenting with LLM-driven trading strategies. My notes and tweaks are tracked in [NOTES.md](NOTES.md).
>
> **My setup:** I primarily run this with the Gemini provider since I have free API credits there. If you're following along, swap `provider` to `"google"` in your config and set `GOOGLE_API_KEY` in your `.env`.
>
> **Tip:** I've found `gemini-2.0-flash` to be a good balance of speed and quality for the analyst agents. For the final trading decision (Portfolio Manager), bumping up to `gemini-2.5-pro` noticeably improves reasoning quality if you have the quota.
>
> **Rate limiting note:** When running multiple analyst agents in parallel with the free Gemini tier, I occasionally hit 429 errors. Setting `max_debate_rounds` to `1` in the config helps reduce API calls significantly during experimentation.
>
> **Backtest tip:** When backtesting over a long date range, set `online_tools` to `False` in the config to avoid hammering live data APIs and to keep results reproducible. I usually pair this with a local CSV of OHLCV data exported from yfinance.
>
> **Ticker watchlist:** My current focus tickers for experimentation are `NVDA`, `MSFT`, and `TSLA` — a mix of high-volatility and steadier names to stress-test the agents across different market conditions.
