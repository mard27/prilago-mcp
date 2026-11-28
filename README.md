# Prilago — Institutional LP Intelligence & Remote MCP Server

**Website:** [https://prilago.com](https://prilago.com) · **LP Directory:** [https://prilago.com/directory](https://prilago.com/directory) · **Try Fund Fit:** [https://prilago.com/demo](https://prilago.com/demo) · **MCP Docs:** [https://prilago.com/mcp](https://prilago.com/mcp) · **Pricing:** [https://prilago.com/pricing](https://prilago.com/pricing) · **GitHub:** [https://github.com/prilago](https://github.com/prilago) · **X:** [https://x.com/prilagohq](https://x.com/prilagohq) · **LinkedIn:** [https://www.linkedin.com/company/prilagohq](https://www.linkedin.com/company/prilagohq)

**Prilago** (`https://prilago.com`, operated by **Prilago LLC**) is a primary-source US institutional Limited Partner (LP) research workspace and remote **Model Context Protocol (MCP)** server built for General Partners raising **Fund I to IV** across Venture Capital, Private Equity, Growth Equity, Private Credit, Real Estate, and Real Assets.

> **Repository scope:** This public repository contains documentation, MCP registry metadata (`server.json`, `glama.json`), and JSON connection configurations for Prilago's hosted remote Streamable-HTTP MCP endpoint (`https://prilago.com/mcp`). No local installation or runtime code is required.

---

## Live Primary-Source Coverage

Every record on [Prilago](https://prilago.com/coverage) traces to an archived public statutory filing (public pension ACFRs and board investment packets, IRS Form 990-PF foundation schedules, university endowment reports, DOL Form 5500 trusts, and SEC Form ADV Part 1A / Section 7.B.1 filings):

- **5,290 Direct Institutional LPs** across 11 allocator segments (`3,597` with disclosed third-party private-market vehicles on file), tracked separately from **2,868 SEC Form ADV Advisers** (`1,492` FoF/OCIO/MFO advisers + `1,376` private-fund managers; `8,158` total filed entities)
- **62,814 Primary Public Disclosure Records** across **45,200** private-market funds and vehicles, semantically separating original capital commitments from IRS Form 990-PF year-end carrying values and SEC Form ADV managed fund assets
- **2,291 Manager LP Rosters** (`/gp/<slug>`) and **73 Retained Investment Consultant & OCIO Firms** (`/consultant/<slug>`)
- **Zero Fabricated Data & Zero Personal PII:** Prilago stores zero personal email addresses or personal phone numbers; every figure links to the underlying filing page
- **Published Transparent Pricing:** **$500/month** flat (`GP Team Pro`, up to 5 team seats, month-to-month cancel anytime, 7-day evaluation included on approved workspace invites) — see [Pricing](https://prilago.com/pricing) and [Platform Comparisons](https://prilago.com/compare)

---

## Connect Any MCP Client to `https://prilago.com/mcp`

Prilago runs a hosted **Streamable-HTTP** MCP server (`2025-03-26` / `2024-11-05`) at `https://prilago.com/mcp`. Tool discovery (`initialize`, `tools/list`) is open; `tools/call` authenticates with a workspace Bearer key (`Authorization: Bearer prilago_mcp_...`) generated at [https://prilago.com/mcp](https://prilago.com/mcp).

### Claude Desktop / Claude Code

```json
{
  "mcpServers": {
    "prilago": {
      "type": "streamable-http",
      "url": "https://prilago.com/mcp",
      "headers": {
        "Authorization": "Bearer YOUR_PRILAGO_MCP_API_KEY"
      }
    }
  }
}
```

### Cursor (`.cursor/mcp.json`) / VS Code / Windsurf

```json
{
  "mcpServers": {
    "prilago-lp-intelligence": {
      "url": "https://prilago.com/mcp",
      "headers": {
        "Authorization": "Bearer YOUR_PRILAGO_MCP_API_KEY"
      }
    }
  }
}
```

---

## Available MCP Tools (`tools/list`)

| Tool | Description |
| :--- | :--- |
| `search_lps` | Search 5,290 direct institutional LPs (Private Foundations, Public & Corporate Pensions, University Endowments, Healthcare Systems, Insurers, Institutional Trusts, and Sovereign Funds) by name, institution type, geography, strategy, or retained investment consultant. |
| `get_lp_360_dossier` | Retrieve the complete Prilago Investor Profile for a Limited Partner: Total AUM, target vs. actual Private Equity / Credit / Real Assets allocation, disclosed pacing plan, retained consultants, named investment-team roles, filed Net IRR / TVPI / DPI figures, repeat GP relationships, and page-cited fund holdings. |
| `match_fund_to_lps` | Find direct institutional LPs proven in primary filings to back early-series funds (Funds I to IV) from managers under $5B AUM in your strategy and check-size band, excluding existing LPs of a reference manager. |
| `get_breaking_lp_signals` | Query Prilago's LP Filing & News Feed across SEC Form D XML filings, primary LP board/ACFR PDFs, and labeled trade-press disclosures for commitments, pacing plans, RFPs, and CIO transitions. |
| `get_gp_peer_lookalikes` | Inspect any General Partner from verified LP disclosures: direct institutional LPs backing their funds, repeat re-up LPs, median disclosed check size, filed performance multiples, and peer GPs. |
| `get_consultant_gatekeeper_clients` | Query Prilago's Investment Consultant & OCIO Graph to map which institutional LPs each consultant (e.g., Meketa, Aksia, StepStone, NEPC, Callan, Cambridge Associates, Verus) advises. |

---

## Public Fundraising Guides, Filing Research & Comparisons

- **Interactive Preview (No Login Required):** [Try Fund Fit (`https://prilago.com/demo`)](https://prilago.com/demo) · [Browse LP Directory (`https://prilago.com/directory`)](https://prilago.com/directory)
- **Emerging Manager & LP Research Guides:**
  - [Who helps emerging managers raise a first or early-series fund?](https://prilago.com/blog/who-helps-emerging-managers-raise-a-first-fund)
  - [How do emerging managers find institutional LPs for Fund I to IV?](https://prilago.com/blog/how-emerging-managers-find-institutional-lps)
  - [Which private foundations have backed Fund I and Fund II vehicles since 2020? (IRS Form 990-PF)](https://prilago.com/blog/foundations-backing-fund-i-ii-by-strategy)
  - [Which investment consultants advise pensions and endowments on emerging managers?](https://prilago.com/blog/consultants-beside-emerging-manager-commitments)
  - [LP re-up rates across a manager's Funds I to III](https://prilago.com/blog/lp-reup-rates-across-funds-i-to-iii)
  - [How do you verify an institutional LP fund commitment from filings?](https://prilago.com/blog/how-to-verify-an-lp-fund-commitment)
  - [How do fund managers get introduced to institutional LPs?](https://prilago.com/blog/how-gps-get-introduced-to-institutional-lps)
  - [What does an institutional LP database cost and how do you choose?](https://prilago.com/blog/what-an-lp-database-costs-and-how-to-choose)
- **Dated Vendor Comparisons (Read November 21, 2026):**
  - [All LP Database Comparisons (`https://prilago.com/compare`)](https://prilago.com/compare)
  - [Prilago vs. Dakota Marketplace](https://prilago.com/compare/dakota-alternative)
  - [Prilago vs. PitchBook](https://prilago.com/compare/pitchbook-alternative)
  - [Prilago vs. Preqin (BlackRock)](https://prilago.com/compare/preqin-alternative)
  - [Prilago vs. FINTRX](https://prilago.com/compare/fintrx-alternative)
  - [Prilago vs. With Intelligence](https://prilago.com/compare/with-intelligence-alternative)
- **Machine-Readable Discovery Endpoints:**
  - Official MCP Registry Manifest: [`https://prilago.com/.well-known/mcp/server.json`](https://prilago.com/.well-known/mcp/server.json) (`com.prilago/lp-intelligence`)
  - MCP Server Card: [`https://prilago.com/.well-known/mcp.json`](https://prilago.com/.well-known/mcp.json)
  - LLM Index: [`https://prilago.com/llms.txt`](https://prilago.com/llms.txt) · [`https://prilago.com/llms-full.txt`](https://prilago.com/llms-full.txt)

---

## License

Documentation and JSON configuration snippets in this repository are licensed under the [MIT License](./LICENSE). Platform data and services at `https://prilago.com` are governed by the [Prilago Terms of Service](https://prilago.com/terms) and [Privacy Policy](https://prilago.com/privacy).
