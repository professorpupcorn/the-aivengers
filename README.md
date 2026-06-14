# AIVENGERS

An AI-powered e-commerce operating system for multi-channel sellers (Amazon, Shopify, TikTok Shop, Walmart, and more). Pairs a unified metrics dashboard with a fleet of specialized AI agents organized as a real company org chart.

## Files

| File | Description |
|------|-------------|
| `AIVENGERS_Dashboard.html` | Self-contained interactive dashboard prototype. Open directly in any browser, no server needed. |
| `handoff.md` | Full project context: decision log, design system, open items, and conventions. |

## Running the Dashboard

Open `AIVENGERS_Dashboard.html` in any modern browser. No build step, no dependencies (fonts load from Google Fonts).

## What Was Built (June 14, 2026)

### Bug fix: nav tooltip z-index
The left rail uses `backdrop-filter: blur`, which creates an isolated stacking context and caused nav tooltips to render behind the dashboard panels. Fixed by adding `position: relative; z-index: 20` to `.rail`, lifting the entire rail stacking context above the content panels.

### Feature: Run Morning Briefing
A button added to the Command Center header that:
- Renders a JARVIS-styled modal summarizing the four headline KPIs (Revenue, Units, Blended TACoS, Net Margin), business health index, top performing product, and any critical alerts.
- Reads the briefing aloud using the browser Web Speech API: British English voice (`en-GB`), low pitch, measured rate for a robotic delivery. The button and orb pulse while speaking.
- Includes Replay and Stop controls in the modal.
- Provides an **Email report** button that opens a pre-filled draft to the operator email address in the local mail client (uses `mailto:` since the prototype is a static file with no backend).

### Git setup and GitHub push
- Initialized a git repository (`main` branch)
- Added `.gitignore` to exclude `.claude/settings.local.json` (personal, machine-specific)
- Connected to `https://github.com/professorpupcorn/the-aivengers`
- Installed and authenticated the GitHub CLI (`gh`)
- Pushed the initial commit

## Design System

| Token | Value |
|-------|-------|
| Space navy | `#080B14` |
| Glass panel | `#0E1422` |
| Arc-reactor cyan | `#36E2FF` |
| Repulsor gold | `#FFB627` |
| Alert red | `#FF3B5C` |
| Success green | `#2EE6A0` |
| Violet | `#9B8CFF` |

Fonts: Space Grotesk (display), Inter (UI), JetBrains Mono (data readouts).

## Conventions

- No em dashes anywhere in copy.
- Product name is **AIVENGERS** (all caps).
- Landed cost is the only value a user ever types in; everything else pulls from connected APIs.
