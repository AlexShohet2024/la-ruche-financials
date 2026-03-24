# La Ruche · Plain-English Financial Model

An interactive, browser-based financial model for **La Ruche** — a vertically integrated wellness ecosystem combining residential co-living, outpatient clinical services, clinical coworking, and a rooftop social club in West Hollywood, California.

**Live site:** [alexshohet2024.github.io/la-ruche-financials](https://alexshohet2024.github.io/la-ruche-financials)

---

## What This Is

This is a single-file HTML application that explains the La Ruche financial model in plain language. It is designed to be shared with investors, partners, and advisors who may not have a finance background. Every assumption is exposed as a live slider — move any slider and every number across all seven tabs updates instantly.

It is not a spreadsheet. It requires no software, no login, and no internet connection after the page loads. Anyone with a web browser can use it.

---

## The Seven Tabs

| Tab | What It Covers |
|-----|---------------|
| 1. The Big Picture | The four revenue streams and why integrating them creates financial advantage |
| 2. How Money Comes In | Bottom-up revenue assumptions with live sliders for clinical occupancy, daily rate, and residential rent |
| 3. Where It Goes | Expense breakdown showing fixed vs. variable costs and why the variable clinical staffing model matters |
| 4. What's Left Over | Plain-English definitions of EBITDA, NOI, Free Cash Flow, and DSCR with live calculations |
| 5. What It's Worth | Two-layer valuation — PropCo (real estate cap rate) and OpCo (EBITDA multiple) — and how investors get their money back |
| 6. Capital Stack | Senior debt, mezzanine, and common equity sliders with live debt service table, DSCR impact, and market context |
| 7. Play With It | Master control panel where all assumptions can be stress-tested simultaneously |

---

## Key Financial Assumptions (Defaults)

| Assumption | Default Value | Range |
|---|---|---|
| Clinical occupancy | 100% (200 clients) | 30%–100% |
| Average daily patient rate | $750/day | $400–$1,200 |
| Residential occupancy | 100% (80 units) | 40%–100% |
| Monthly rent per unit | $3,438 | $2,000–$5,000 |
| Expense ratio | 61.5% of revenue | 50%–80% |
| Senior LTC | 63% | 40%–75% |
| Mezzanine | 0% | 0%–20% |
| Senior debt rate | 6.50% | 4.5%–9.0% |
| Mezzanine rate | 12.0% (interest-only) | 8%–16% |
| PropCo cap rate | 6.0% | 4.5%–8.0% |

---

## Year 3 Stabilized Outputs (at defaults)

| Metric | Value |
|---|---|
| Total annual revenue | ~$30.0M |
| EBITDA | ~$11.5M |
| EBITDA margin | ~38% |
| PropCo NOI | ~$7.0M |
| Free cash flow | ~$8.5M |
| DSCR | ~2.35× |
| Enterprise value | $183M–$212M |
| Common equity required | $29.0M |

---

## The Four Revenue Streams

**Heal — Treatment Clinic** `$18.75M`
Up to 200 clients receiving addiction and mental health treatment. Revenue from insurance reimbursement and private pay. Staffing is contracted per patient (variable cost model), not salaried.

**Live — Co-Living Apartments** `$3.3M`
80 furnished residential units at West Hollywood market rates (~$3,438/month average). Premium justified by integrated wellness services.

**Work — Wellness Mall** `$4.0M`
25,000 sq ft of clinical offices, therapy rooms, fitness, longevity services, and a cafe. Providers lease space fractionally by the hour, day, or month.

**Play — Rooftop Social Club** `$3.9M`
12,000–15,000 sq ft rooftop with pool, restaurant, and event space. Membership-based ($2K–$10K/year) plus food and beverage revenue.

---

## Capital Stack (Default vs. Market Reality)

The default model assumes 63% senior LTC with no mezzanine — achievable but optimistic for a mixed-use behavioral health asset in today's lending environment. A more conservative market-realistic stack would be:

| Layer | Default | Conservative Case |
|---|---|---|
| Senior debt | 63% ($49.5M) @ 6.5% | 50–55% @ 6.5–7.5% |
| Mezzanine | 0% | 8–15% @ 10–14% |
| Common equity | 37% ($29.0M) | 30–42% |

Use Tab 6 to model the impact of adding mezzanine debt. The DSCR warning on Tab 6 triggers if the capital structure falls below the 1.25× bank minimum.

---

## How to Update the Model

1. Download `index.html` from this repository
2. Open it in any text editor (Notepad, TextEdit, VS Code, etc.)
3. Make changes to the content
4. Save the file
5. Upload it back to this repository, replacing the existing `index.html`
6. GitHub Pages will republish within 60–90 seconds

To change a **default slider value**, find the relevant `<input type="range">` element and update its `value=""` attribute. For example, to change the default clinical occupancy from 100% to 80%:

```html
<!-- Find this -->
<input type="range" min="0.3" max="1.0" value="1.0" ...>

<!-- Change to -->
<input type="range" min="0.3" max="1.0" value="0.8" ...>
```

---

## Technical Notes

- **Single file.** The entire application — HTML, CSS, and JavaScript — is contained in one `index.html` file. No build process, no dependencies, no server required.
- **No external data.** All calculations happen in the browser using vanilla JavaScript. No API calls are made after the Google Fonts stylesheet loads.
- **Fully offline after first load.** Once the page has loaded, it works without an internet connection (except for the Google Fonts typeface, which degrades gracefully to a system serif font).
- **Mobile responsive.** The layout adapts for screens smaller than 800px. Header KPIs are hidden on mobile; the tab bar scrolls horizontally.
- **No frameworks.** Pure HTML, CSS, and JavaScript. Compatible with all modern browsers.

---

## Sources

- La Ruche source deck (internal, 2023)
- CBRE Multifamily Innovation Watch: The Rise of Co-Living
- Reconciled financial model (March 2026)
- Commercial real estate lending market data, Q1 2026

---

## Disclaimer

This model is for discussion purposes only. All projections are based on assumptions that are subject to change. Past performance of comparable assets does not guarantee future results. This does not constitute investment advice. Prospective investors should conduct their own due diligence and consult qualified financial, legal, and tax advisors before making any investment decision.

---

*La Ruche · West Hollywood, California · evergreenfund.life*
