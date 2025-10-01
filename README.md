# Trade It MCP Server
(previously known as Trade Agent)

<a href="https://glama.ai/mcp/servers/@Trade-Agent/trade-agent-mcp">
  <img width="380" height="200" src="https://glama.ai/mcp/servers/@Trade-Agent/trade-agent-mcp/badge" />
</a>

**Endpoint:**  `https://mcp.tradeit.app/sse`  
**Mode:** Remote-only (no local deployment required)

## Overview

The Trade It MCP Server brings stock and crypto trading support to agents. It enables natural-language interaction with stock and crypto brokerages—execute trades, query portfolio performance, and surface market insights by sending plain-English requests through the MCP protocol.

Supports Charles Schwab, Robinhood, E*TRADE, Webull, Coinbase, and Kraken. More to be added soon!

This server is **remote** so you don't need to run anything locally to connect. Just point your MCP-compatible agent platform to the URL above.

---

## Tools

- 💬 **Create Trade**
  Creates a trade order to buy or sell an asset.

  ORDER TYPES:
  - **market** (default) → Executes immediately at current market price. No price fields required.
  - **limit** → Executes only at a specific limit_price or better. Requires `limit_price`.
  - **stop** → Triggers a market order when stop_price is reached. Requires `stop_price`.
  - **stop_limit** → Triggers a limit order when stop_price is reached. Requires BOTH `stop_price` and `limit_price`.
 
  EXAMPLES:
  - "Buy $1000 of Tesla"
  - "Buy $1000 of Tesla, but only if the price drops to $150 or lower"
  - "Sell 10 shares of Apple if the price falls to $140 or lower"
  - "Buy a share of Apple if it hits $200"
  - "Buy 10 shares of Apple if the price rises to $140, but don't pay more than $142 per share"

  DEFAULTS:
  - If no amount is given, your default amount is used.
  - If no account is given, your default account is used. 
  - If no order type is given, the trade is a market order. 
  - If auto-execute is enabled in settings, the trade will execute immediately. Otherwise, it gets created in draft state and requires a call to `Execute Trade` to complete. This allows you to review and confirm trades.

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

- 🔍 **COMING SOON: Copy Trading**  
  Example: `"Put $1000 in Nancy Pelosi's portfolio."`

---

## Getting Started

1. First, create an account at https://tradeit.app.
2. Sign up for the Pro plan's free trial.
3. Connect your brokerage of choice.

## Connecting
1. Connect your MCP client to `https://mcp.tradeit.app/sse`.
2. Authenticate through the browser-based OAuth flow.
3. You're now ready to start trading!
