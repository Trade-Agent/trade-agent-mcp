# Trade Agent MCP Server

<a href="https://glama.ai/mcp/servers/@Trade-Agent/trade-agent-mcp">
  <img width="380" height="200" src="https://glama.ai/mcp/servers/@Trade-Agent/trade-agent-mcp/badge" />
</a>

**Endpoint:**  `https://mcp.thetradeagent.ai/sse`  
**Mode:** Remote-only (no local deployment required)

## Overview

The Trade Agent MCP Server brings stock and crypto trading support to agents. It enables natural-language interaction with stock and crypto brokerages—execute trades, query portfolio performance, and surface market insights by sending plain-English requests through the MCP protocol.

Supports Charles Schwab, Robinhood, E*TRADE, Webull, Coinbase, and Kraken. More to be added soon!

This server is **remote** so you don't need to run anything locally to connect. Just point your MCP-compatible agent platform to the URL above.

---

## Tools

- 💬 **Create Trade**
  Draft a trade order for review before submitting.
  Example: `"Buy $500 of Apple"` or `"Sell 10 shares of SPY"`

- 💬 **Execute Trade**
  Execute the trade on your brokerage.

- 💬 **Show Account Details**
  List your linked brokerages along with their current value and cash balance.
  Example: `"Show my accounts"`

- 💬 **Search Asset**
  Get current price and metadata for any stock or cryptocurrency.
  Example: `"How's Apple doing?"` or `"What's the price of TSLA?"`

- 📊 **COMING SOON: Portfolio Queries**  
  Example: `"How is my portfolio doing?"` or `"What’s my exposure to tech?"`

- 🔍 **COMING SOON: Market Queries**  
  Example: `"How is Berkshire performing relative to the S&P?"`

- 🔍 **COMING SOON: Copy Trading**  
  Example: `"Put $1000 in Nancy Pelosi's portfolio."`

---

## Getting Started

1. First, create an account at https://thetradeagent.ai.
2. Sign up for the Pro plan's free trial.
3. Connect your brokerage of choice.

## Connecting
1. Connect your MCP client to `https://mcp.thetradeagent.ai/sse`.
2. Authenticate through the browser-based OAuth flow.
3. You're now ready to start trading!
