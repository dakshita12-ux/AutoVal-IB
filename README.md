# AutoVal-IB: Automated DCF Valuation & M&A Pitchbook Engine

[![Live Web App](https://img.shields.io/badge/Live_App-Interactive_Pitchbook-blue?style=for-the-badge&logo=github)](https://dakshita12-ux.github.io/AutoVal-IB/)

**AutoVal-IB** is an executive-level interactive valuation and M&A modeling dashboard engineered for Investment Banking transaction analysis. It automates key corporate finance workflows including 3-Stage Discounted Cash Flow (DCF) valuation, dynamic sensitivity modeling, trading comps peer benchmarking, and M&A accretion/dilution deal structuring.

---

## 🚀 Live Demo
Access the interactive web application here:  
**👉 [https://dakshita12-ux.github.io/AutoVal-IB/](https://dakshita12-ux.github.io/AutoVal-IB/)**

---

## 🏗️ System Architecture & Financial Data Pipeline

┌─────────────────────────────────────────────────────────────────────────────┐
│                             INPUT PARAMETERS                                │
│  - Financial Metrics (Revenue, EBIT, CapEx, Total Debt, Cash, Shares Out)    │
│  - Cost of Capital Inputs (Risk-Free Rate, Beta, Market Risk Premium)       │
│  - M&A Deal Parameters (Target Premium, Cash/Stock Mix, Synergies, Debt Rate)│
└────────────────────────────────────┬────────────────────────────────────────┘
│
▼
┌─────────────────────────────────────────────────────────────────────────────┐
│                         VALUATION PROCESSING ENGINE                         │
│                                                                             │
│  ┌──────────────────────┐  ┌──────────────────────┐  ┌────────────────────┐ │
│  │     CAPM & WACC      │  │     3-STAGE DCF      │  │   TRADING COMPS    │ │
│  │  Ke = Rf + β*(Rm-Rf) │  │ 5-Yr FCFF Forecast   │  │ EV/EBITDA, P/E,    │ │
│  │  Dynamic Debt Shield │  │ Terminal Value (TV)  │  │ EV/Revenue Bench   │ │
│  └──────────┬───────────┘  └──────────┬───────────┘  └─────────┬──────────┘ │
│             │                         │                        │            │
│             └─────────────────────────┼────────────────────────┘            │
│                                       ▼                                     │
│                        ┌──────────────────────────────┐                     │
│                        │ M&A ACCRETION / DILUTION     │                     │
│                        │ Pro-Forma Income Statement   │                     │
│                        │ Post-Merger EPS Reconciliation│                    │
│                        └──────────────┬───────────────┘                     │
└───────────────────────────────────────┼─────────────────────────────────────┘
│
▼
┌─────────────────────────────────────────────────────────────────────────────┐
│                            EXECUTIVE DASHBOARD                              │
│  - Implied Target Share Price & Enterprise Value Bridge                     │
│  - Dynamic 2D Sensitivity Heatmap (WACC vs. Terminal Growth)               │
│  - Relative Valuation Peer Charts & M&A EPS Impact Summary                  │
└─────────────────────────────────────────────────────────────────────────────┘


---

## 🔑 Key Features & Financial Modules

### 1. 📊 3-Stage Discounted Cash Flow (DCF) Engine
* **CAPM Cost of Equity:** Calculates $R_e$ dynamically using Risk-Free Rate ($R_f$), Beta ($\beta$), and Equity Risk Premium ($ERP$).
* **WACC Recalculation:** Re-levers capital structures and incorporates tax shields ($(1 - T)$).
* **5-Year FCF Projections:** Forecasts Unlevered Free Cash Flows ($FCFF$) with explicit revenue growth and EBIT margin parameters.
* **Terminal Value:** Dual calculation using Perpetual Growth Rate and Exit Multiple methodologies.

### 2. 🎛️ 2D Valuation Sensitivity Matrix
* Interactive 5x5 heatmap evaluating implied target share price variations across dynamic **WACC vs. Terminal Growth Rate** ranges.

### 3. 📈 Trading Comps & Peer Benchmarking
* Automated peer comparison matrix assessing relative valuation metrics:
  * **$EV / EBITDA$**
  * **$P / E$**
  * **$EV / Revenue$**
* Visual bar charts highlighting valuation positioning relative to peer medians.

### 4. 🤝 M&A Accretion / Dilution Analysis
* Strategic deal structuring evaluating post-transaction EPS impact.
* Custom consideration mix: **Cash % vs. Stock %**.
* Inputs for target acquisition premium, debt financing interest rates, and post-merger cost synergies.
* Full post-merger pro-forma income statement reconciliation bridge.

---

## 🛠️ Tech Stack & Dependencies
* **Frontend:** Vanilla HTML5, CSS3 (Flexbox & CSS Grid), JavaScript (ES6+)
* **Data Visualization & Charts:** Chart.js
* **Deployment & Hosting:** GitHub Pages

---

## 📌 Usage for Pitchbook Presentations
1. Navigate to the **[Live Dashboard](https://dakshita12-ux.github.io/AutoVal-IB/)**.
2. Adjust underlying financial drivers and transaction assumptions in the left control panel.
3. Review updated intrinsic share prices, Football Field valuation bridges, sensitivity matrices, and pro-forma M&A EPS accretion/dilution figures in real time.
