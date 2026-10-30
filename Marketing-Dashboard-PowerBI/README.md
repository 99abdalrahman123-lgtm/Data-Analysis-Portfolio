# 📊 Marketing Campaign Performance Dashboard

**Power BI · DAX · Star Schema · Custom Design System**

An interactive Power BI report that turns **200K marketing campaigns** into clear answers for two audiences. Executives get a one-screen view of spend, return and conversion efficiency. Campaign teams get a company-level deep-dive to decide where the next dollar should go.

---

## 🎯 Business Problem

Marketing budgets were spread across **5 companies, 6 channels and 5 campaign types** without a single view of what actually pays back. The report answers:

- **Where is the budget going, and is it earning a return?** Spend vs. ROI by month, campaign type and city.
- **Which channels convert, and which only attract clicks?** CTR, the Impressions → Clicks → Conversions funnel, and conversions vs. the channel average.
- **Which campaigns should we scale or cut?** Cost vs. conversion scatter, and Company × Campaign Type performance.
- **Does high engagement turn into sales?** Quarterly engagement vs. conversion trend.
- **Which audiences and languages are most profitable?** ROI heatmap by Language × Customer Segment.

---

## 🧭 Report Pages

| Page | Audience | What it shows |
|---|---|---|
| **Intro** | Everyone | Landing page with navigation to both dashboards |
| **Executive Overview** | Leadership | 6 KPIs (Spend, Revenue, ROI, Conversions, CTR, CPC), spend vs. ROI trend, budget split, conversions decomposition tree, city map, CTR by channel, marketing funnel |
| **Company Deep-Dive** | Campaign & ops teams | Company slicer, 6 operational KPIs (Campaigns, Conversion Rate, CPA, Engagement, Duration, Top ROI Channel), scatter, performance matrix, cost tiers, ROI heatmap, engagement vs. conversion |

---

## 🛠️ How It's Built

- **Data model:** a star schema with 1 fact table (`Fact_Campiagnes`) and 6 dimensions (Date, Channel, Company, Audience, Geography, Cost Tiers), plus a dedicated `_Measures` table.
- **DAX:** KPI measures for ROI, CTR, CPC, CPA and Revenue, and a variance-to-average measure that makes small differences between channels visible.
- **UX:**
  - **Navigation:** a side menu that moves between pages and a Reset button that clears all slicers.
  - **Interaction:** tooltips on every chart, cross-filtering, and a drill-down decomposition tree.
  - **Colour:** heatmaps and bars use colour gradients, so close values are still easy to tell apart.
- **Design system:** a custom **Eldatawy · Data Wizard** theme in dark navy and cyan. It sets the background, panel and accent colours (`#01122A` / `#001A38` / `#04FBFE`) for every page, card and tooltip.

---

## 🚀 Getting Started

1. Install the latest [Power BI Desktop](https://powerbi.microsoft.com/desktop/).
2. Download `Marketing_Dashboard.pbix` and open it.
3. Start on the **Intro** page. In Desktop, hold **Ctrl + Click** to use the navigation buttons.

```
├── Marketing_Dashboard.pbix   # Power BI report + data model
├── theme/                     # Eldatawy Data Wizard theme (JSON)
├── intro-page/                # HTML/CSS/JS landing page
└── README.md
```

---

## 👤 Author

**Omar Sherif** · *Eldatawy – Data Wizard*
Data Analyst · Power BI Developer
