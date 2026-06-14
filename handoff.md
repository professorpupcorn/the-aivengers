# AIVENGERS — Project Handoff

_Last updated: June 14, 2026_

## What this is

AIVENGERS is an AI-powered e-commerce operating system for multi-channel sellers (Amazon, Shopify, TikTok Shop, Walmart, etc.). It pairs a unified metrics dashboard with a fleet of specialized AI agents organized like a real company org chart. There are two deliverables in this project so far: a written PRD and a working dashboard prototype.

## Deliverables (current state)

| File | What it is | Status |
|------|-----------|--------|
| `AIVENGERS_PRD_v1.0.docx` | Full product requirements document, 19 sections | Complete |
| `AIVENGERS_Dashboard.html` | Interactive futuristic dashboard prototype (self-contained, single file) | Working prototype |
| `handoff.md` | This file | — |

There is also an older `Nexus_PRD_v1.0.docx` floating around — that was the original draft before the rename. The current PRD is the **AIVENGERS** one.

## How we got here (decision log)

1. Started from two source PDFs: the **DST Metrics Cheat Sheet** (Titan Network's daily sales tracking framework) and a **Stage 4 Org Chart** (roles/responsibilities at $10MM/year).
2. Built a PRD for an AI assistant + dashboard product. Originally named **Nexus**.
3. Renamed the product from Nexus to **AIVENGERS** (all 17 instances replaced).
4. Removed all em dashes (58 of them) and reformatted with colons, semicolons, and commas per request. **Keep this constraint going — no em dashes in any future copy.**
5. Built the dashboard prototype with a "Tony Stark / JARVIS HUD" aesthetic.

## The PRD at a glance

19 sections covering: Executive Summary, Product Overview, Onboarding (connect APIs, import products, enter landed cost as the only manual input), Platform Architecture, Master Command Center, Daily Sales Tracker, Inventory & Supply Chain, Projects & Tasks, Marketing & Advertising, AI Agent System, Reviews & Reputation, Financial P&L, Product Development, Integrations & API, User Roles, Technical Requirements, Pricing Tiers, Phased Roadmap, and Success Metrics.

Key product principles baked in:
- **Landed cost is the only thing a user ever types in.** Everything else pulls from connected APIs.
- **Trend lines over snapshots** — the DST philosophy from the cheat sheet.
- **Agents act, not just report**, with three autonomy levels: Advise / Assist / Autopilot.
- **Agent hierarchy mirrors the Stage 4 org chart** — six department managers, each with specialist sub-agents.

## The dashboard prototype

Single self-contained `AIVENGERS_Dashboard.html` file (~50KB, no external dependencies except Google Fonts). Open it directly in any browser.

**Design system:**
- Palette: deep space navy `#080B14`, glass panels `#0E1422`, arc-reactor cyan `#36E2FF`, repulsor gold `#FFB627` (carried over from the original Titan brand gold), alert red `#FF3B5C`, success green `#2EE6A0`, violet `#9B8CFF`.
- Type: Space Grotesk (display), Inter (UI), JetBrains Mono (data readouts).
- Signature element: animated **arc-reactor business-health ring** on the Command Center.
- Respects `prefers-reduced-motion`; responsive down to mobile.

**Six views (switchable via the left rail):**
1. **Command Center** — KPI tiles with sparklines, the health reactor + sub-gauges, alert tray, agent activity feed, top products.
2. **Daily Sales Tracker** — multi-series trend chart + all metric groups from the cheat sheet (Traffic & Conversion, Total Sales, Organic Split, PPC, TACoS, Reviews) with values, deltas, targets.
3. **Inventory & Supply Chain** — stock table with days-of-cover bars, AI-drafted reorder queue, in-transit tracking, revenue-at-risk callout.
4. **Marketing & Advertising** — channel cards, PPC campaign efficiency, influencer pipeline.
5. **Projects & Tasks** — kanban board + launch phase tracker.
6. **Agent Roster** — six department managers, sub-agents, autonomy toggles.

Plus a persistent **JARVIS assistant bar** (types out briefings) and a live status ticker.

All data in the prototype is **hardcoded mock data** (see the data objects near the top of the `<script>`: `SKUS`, `DST`, `ALERTS`, `FEED`, `INV`, `CHANNELS`, `TASKS`, `AGENTS`).

## Open items / next steps

These were proposed but not yet built:
- [ ] Wire the time-range chips (7D / 30D / 90D) on the DST view to actually re-render the chart with different data.
- [ ] Wire the SKU selector dropdown on the DST view so switching products updates all metrics (only one SKU has full DST data right now).
- [ ] Add a 7th view for the **Financial P&L** dashboard (it's in the PRD but not in the prototype).
- [ ] Make the JARVIS bar a real input (currently display-only; the `⌘K` key hint is decorative).

Other possible directions not yet discussed:
- Reviews & Reputation and Product Development dashboards exist in the PRD but not the prototype.
- Connect to real APIs / replace mock data.
- Build out the onboarding flow.

## Conventions to remember

- **No em dashes** anywhere in copy.
- Product name is **AIVENGERS** (all caps).
- Keep the gold lineage to the original Titan brand.
- Reasonably concise tone.

## Files location

All current deliverables are in the outputs directory:
- `AIVENGERS_PRD_v1.0.docx`
- `AIVENGERS_Dashboard.html`
- `handoff.md`
