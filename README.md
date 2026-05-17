# 🏦 Intelli-Credit — AI-Powered Credit Appraisal Engine

> An AI-first credit management platform for Indian NBFCs, banks, and lending institutions. Built with React + Vite.

![Intelli-Credit Dashboard](https://via.placeholder.com/1200x600/040812/22d3ee?text=Intelli-Credit+Dashboard)

## ✨ Features

### 🏠 Command Center (Dashboard)
- Live market ticker (NIFTY, SENSEX, RBI Repo, GSec yields)
- Real-time KPI cards: Total applications, approvals, declines, avg credit score
- Portfolio sector mix (donut chart)
- Application status split
- Monthly sanctions vs disbursement (bar chart)
- Risk grade distribution
- Portfolio health radar chart

### 📋 Applications Pipeline
- Full CRUD pipeline for 10+ Indian companies across sectors
- Filter by status: All / Approved / Pending / Declined
- Search by company name or sector
- Credit score gauge with DSCR/grade indicators
- Expandable verdict / decline rationale cards

### 🔍 Application Detail Modal (8 Tabs)
| Tab | Contents |
|-----|----------|
| **Overview** | Credit score gauge, financials, loan terms, verdict box |
| **Financials** | Revenue/EBITDA/PAT area charts, ratio KPIs, bar comparisons |
| **GST** | GSTR-2A reconciliation, circular trading AI detection |
| **Forensic** | Round-tripping detection, RPT analysis, bank statement heatmap |
| **Legal** | Litigation registry, e-courts data, regulatory compliance matrix |
| **Collateral** | Coverage donut, quality score bars, title clearance |
| **Promoter** | Character radar, background screening, news sentiment |
| **CAM** | Sanction letter preview, downloadable CAM / Sanction / Term Sheet |

### 📑 CAM Document Repository
- Download Credit Appraisal Memos (.txt)
- Sanction Letters
- Term Sheets

### 🧾 GST Reconciliation Engine
- GSTR-2A vs 3B cross-verification
- Quarterly match rate trend charts
- AI circular trading detection with severity classification

### 🔬 Forensic Layer
- Related party transaction (RPT) analysis
- Cash withdrawal pattern detection
- Round-tripping detection (MCA director network)
- Benami transaction screening
- AML / KYC compliance checks

### 🧠 Explainability (XAI)
- Interest rate decomposition (MCLR + spread build-up)
- Score factor breakdown with weighted contributions
- Decision radar chart
- AI audit trail with step-by-step timing

### ⚖️ Legal & Litigation
- e-Courts monitoring
- NCLT / DRT / High Court tracker
- Regulatory compliance matrix (ROC, IT, GST, FEMA)

### 🏛️ Collateral Engine
- Coverage % vs 125% threshold
- Collateral type distribution (immovable / movable / financial)
- Quality scores: title, encumbrance, insurance, liquidity

### 👤 Promoter Intelligence
- 360° background screening
- Character radar (track record, CIBIL, compliance)
- Web-scale news sentiment scan

### 🔭 Research Agent
- RBI policy monitor
- e-Courts & NCLT feed
- Macro & sector intelligence

### 💱 FX Converter
- 10-currency converter (INR, USD, EUR, GBP, SGD, AED, JPY, CNY, CHF, AUD)
- Live FX rate table

### 📊 Portfolio Analytics
- Score distribution donut
- Sector exposure (₹ Cr)
- Leverage vs credit score scatter
- NPA risk heatmap

### 🤖 IntelliBot (AI Agent)
- Built-in floating AI chat assistant
- Context-aware answers about all 10 applications
- Knowledge base: GST, forensic, RBI policy, CIBIL, rates
- Quick-action buttons for common queries
- Typing indicator animation

---

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- npm 9+

### Installation

```bash
git clone https://github.com/your-username/intelli-credit.git
cd intelli-credit
npm install
npm run dev
```

App runs at **http://localhost:3000**

### Build for Production

```bash
npm run build
npm run preview
```

---

## 🗂️ Project Structure

```
intelli-credit/
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── AIAgent.jsx          # Floating AI chat assistant
│   │   ├── AppModal.jsx         # 8-tab application detail modal
│   │   ├── Charts.jsx           # SVG chart components (Pie, Radar, Area, Gauge, Bar)
│   │   ├── Pages.jsx            # All page components (Dashboard, Applications, etc.)
│   │   └── UI.jsx               # Shared primitives (StatusBadge, RiskBadge, SectionHead)
│   ├── data/
│   │   ├── aiKnowledgeBase.js   # IntelliBot Q&A knowledge base
│   │   ├── companies.js         # Mock credit application dataset (10 companies)
│   │   └── constants.js         # Nav config, FX rates
│   ├── styles/
│   │   └── globalStyles.js      # CSS-in-JS global styles + CSS variables
│   ├── utils/
│   │   └── camGenerator.js      # CAM / Sanction / TermSheet document generators
│   ├── App.jsx                  # Root app shell (sidebar, topbar, routing)
│   └── main.jsx                 # React entry point
├── index.html
├── vite.config.js
├── package.json
└── README.md
```

---

## 🎨 Design System

| Variable | Value | Usage |
|----------|-------|-------|
| `--c1` | `#22d3ee` | Cyan — primary actions, borders |
| `--c2` | `#a78bfa` | Violet — AI, secondary elements |
| `--c3` | `#34d399` | Green — approved, positive |
| `--c4` | `#fbbf24` | Amber — pending, warnings |
| `--c5` | `#f87171` | Red — declined, critical |
| `--ink` | `#040812` | Background (deep navy) |
| `--font` | Outfit | Body font |
| `--disp` | Fraunces | Display / heading font |
| `--mono` | Space Mono | Numbers, IDs, codes |

---

## 📦 Sample Dataset

10 synthetic Indian companies across sectors:

| Company | Sector | Amount | Status | Score |
|---------|--------|--------|--------|-------|
| Tata Nexgen Infra Ltd | Infrastructure | ₹450 Cr | ✅ Approved | 78 |
| IndoSolar Energy Systems | Renewable Energy | ₹320 Cr | ✅ Approved | 83 |
| Bharat Agro Foods Ltd | FMCG | ₹210 Cr | ✅ Approved | 76 |
| Ananta Textile Industries | Textile | ₹140 Cr | ✅ Approved | 71 |
| Zenith Pharma Exports | Pharmaceuticals | ₹180 Cr | ⟳ Pending | 61 |
| Metro Logistics Chain | Logistics | ₹95 Cr | ⟳ Pending | 55 |
| Himalaya Auto Components | Auto Components | ₹175 Cr | ⟳ Pending | 67 |
| Bright Steel MSME Works | Manufacturing | ₹25 Cr | ❌ Declined | 38 |
| NovaTech IT Solutions | IT/ITES | ₹60 Cr | ❌ Declined | 44 |
| Coastal Fisheries Co-op | Agri & Fisheries | ₹45 Cr | ❌ Declined | 41 |

---

## 🛠️ Tech Stack

- **React 18** — UI framework
- **Vite 5** — Build tool & dev server
- **Pure CSS-in-JS** — No CSS framework dependencies
- **Custom SVG charts** — PieChart, RadarChart, AreaChart, GaugeChart, BarChart (no chart library needed)
- **Google Fonts** — Outfit, Space Mono, Fraunces

---

## 📄 License

MIT License — free to use, modify and distribute.

---

## 🙏 Credits

Built as a demonstration of AI-powered fintech tooling for Indian credit markets. All company data is entirely fictional and for demonstration purposes only.
