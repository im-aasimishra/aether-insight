# AetherInsight - Executive Technical Architecture Overview

This document provides a clean, visual, and non-technical explanation of the **AetherInsight** system architecture. Use this guide to explain the technology stack, logical decisions, and data pipelines clearly to stakeholders, team leads, or hackathon judges.

---

## 1. Core Technological Stack: "What" & "Why"

| Technology | What it does in AetherInsight | Why we use it (The Business Value) |
| :--- | :--- | :--- |
| **React (Vite)** | Orchestrates components, manages page transitions, and coordinates state hooks. | React allows for immediate rendering. Vite compiles our bundle in 1.2 seconds, avoiding heavy webpack configurations. |
| **CSS3 (Custom Theme)** | Defines the premium Frosted Aurora & Champagne Gold light theme variables and animations. | A highly custom, bright corporate palette stands out immediately from generic dark-mode templates. |
| **Recharts API** | Draws dynamic SVG trend curves and domain density charts. | Provides lightweight, native visual charting with smooth mouseover animations. |
| **HTML5 FileReader** | Ingests `.csv`, `.json`, and `.txt` records locally in the client browser. | Guarantees data privacy. User spreadsheets are processed in-memory client-side without leaving their computer. |

---

## 2. Standout Innovation: "Neural Flow Sandbox Router"

AetherInsight stands out from typical static dashboards through our **Interactive Neural Sandbox**:
- **Simulating AI Pipelines in Real-Time:** Users type any review phrase (e.g., *"battery drain is fast"*).
- **Physical Particle Pathing:** An SVG vector track animates a glowing data particle across the dashboard.
- **Pipeline Gates:** The particle pauses at evaluation gates (Typos Cleaned ➔ Sentiment Judged ➔ Domain Inferred).
- **Dynamic Bucket Accumulation:** The particle drops into a category card, triggering a champagne gold ripple and incrementing variables in real-time.

---

## 3. Data Pipeline Flow: "How it Works"

```
[ RAW FILE / DRAG & DROP ] (Phase 1)
           │
           ▼
[ CSV/JSON LINE READERS ] ➔ Standardizes objects, maps key parameters.
           │
           ▼
[ FUZZY DEDUPLICATOR ] (Phase 2) ➔ Evaluates string distances (Levenshtein Distance)
           │                        to merge contact typos (e.g. "J. Smith" vs "John Smith").
           ▼
[ ATTRIBUTE INFERENCING ] ➔ Scans tokens to fill empty category columns.
           │
           ▼
[ NLP LEXICON SCORING ] ➔ Counts positive/negative terms to judge customer sentiment.
           │
           ▼
[ 2D VECTOR CLUSTERING ] (Phase 3) ➔ Scatter positions calculated using sin/cos offsets
           │                         to group similar records in colored target regions.
           ▼
[ ANOMALY RADAR ] ➔ Triggers alarms if negative volume spikes on a single date.
           │
           ▼
[ CATEGORY LEDGER & DASHBOARD ] (Phase 4 & 5) ➔ Renders Area Trends, Bar graphs, and actionable hotfix proposals.
```
