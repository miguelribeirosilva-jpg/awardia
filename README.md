# Awardia

**Tender intelligence for AI agents.** Awardia is a remote MCP server with European public procurement data: open tenders, award history, competitor profiles and bid intelligence. It's updated every night from TED (Tenders Electronic Daily).

🌐 https://awardia.app · 🔌 `https://awardia.app/mcp` · ✉️ hello@awardia.app

> **Free during beta.** No account or API key needed (up to 200 calls per user per day).

## Connect

Add `https://awardia.app/mcp` as a remote MCP server (Streamable HTTP) in your AI app or agent framework, with no authentication.

**Claude:** Settings → Connectors → Add custom connector → paste the URL.

**Clients that only support local servers:**
```json
{
  "mcpServers": {
    "awardia": {
      "command": "npx",
      "args": ["-y", "mcp-remote", "https://awardia.app/mcp"]
    }
  }
}
```

## What you can ask

- "Find open school renovation tenders in Portugal."
- "For tender 673746-2026: how many competitors should I expect and what price usually wins?"
- "Which public IT contracts in Spain end in the next 6 months, and who holds them?"
- "We install solar panels for municipalities. Which open EU tenders fit us?"

## Tools

| Tool | What it does |
|---|---|
| `get_coverage` | What data is available: countries, dates, counts |
| `search_tenders` | Open tenders by keywords (any language), country, CPV sector, value |
| `match_company` | Describe a company in plain words, get tenders it could bid on |
| `award_history` | Who won past contracts, at what price, against how many bidders |
| `expiring_contracts` | Contracts ending soon, with the incumbent supplier, before the re-tender |
| `competitor_profile` | What a company wins: buyers, sectors, value, competition |
| `bid_intelligence` | For a tender: expected bidders, likely winning price range, incumbents, comparable awards |

## Data

- **Source:** contract and award notices from [TED](https://ted.europa.eu), the EU's official public procurement journal.
- **Coverage:** open tenders for the whole EU and EEA, plus two years of award history for Portugal and Spain, with more countries coming.
- **Languages:** search works across languages through the EU Common Procurement Vocabulary (CPV).

Contains data from TED, © European Union, reused under the Commission's reuse policy. Data is provided as is: always confirm details on the official notice before bidding.

## Privacy

For each call we record the tool, its parameters, the client app name and an anonymous code. That code is derived one-way from the caller's IP address and the current month, and can't be reversed. There are no accounts, no cookies and no tracking.

## Contact

hello@awardia.app
# awardia
