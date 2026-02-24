# MoneyMind-Personal-Finance-Teacher---Spanish
# MoneyMind ES v1.0 — Project Reference (English)

**Tu Camino Financiero** · Spanish Edition · Guadalajara, Mexico

---

## What This Is

MoneyMind ES is a personal finance education web app built for a specific person: a 28-year-old chemical engineer with mixed income (salary + reselling), living with his partner in Guadalajara, who regularly supports family financially, and who has clear goals around financial stability and eventually passive income.

It is not a generic personal finance app translated into Spanish. Every module, scenario, example number, and "Seamos Honestos" (Real Talk) section was written with that specific context in mind.

**Base:** Forked from MoneyMind v1.3. All UI strings, module content, quiz data, scenario feedback, tips, and badge names have been replaced with Spanish equivalents. Three entirely new ES-exclusive modules were added that have no equivalent in v1.3.

---

## Module Structure

The app has 5 learning layers that unlock progressively.

### Layer 1 — Fundamentos / Foundation (required, sequential)

| ID | Spanish Title | English Summary | XP | Time |
|----|--------------|-----------------|-----|------|
| l1m1 | Más gasto que ingreso | Spending more than you earn | 50 | 5 min |
| l1m2 | Presupuestar con ingreso variable | Budgeting with variable resale income | 60 | 7 min |
| l1m3 | El presupuesto mensual honesto | Honest monthly budget (with calculator) | 65 | 8 min |
| l1m4 | Los cargos automáticos invisibles | Invisible automatic charges | 55 | 6 min |

### Layer 2 — Herramientas / Applied Tools (interactive calculators)

| ID | Spanish Title | English Summary | XP | Time |
|----|--------------|-----------------|-----|------|
| l2m1 | Calculadora de pago de deuda | Debt payoff calculator (BBVA monthly rate) | 70 | 5 min |
| l2m2 | Tu colchón de ingreso | Income buffer calculator | 70 | 5 min |
| l2m3 | El costo real de vivir juntos | True cost of shared living calculator | 70 | 7 min |

### Layer 3 — Conceptos / Deep Concepts

| ID | Spanish Title | English Summary | XP | Time |
|----|--------------|-----------------|-----|------|
| l3m1 | Construir un fondo de emergencia | Building an emergency fund ($5K MXN goal) | 75 | 6 min |
| l3m2 | Tu tarjeta BBVA por dentro | BBVA credit card: rates, minimums, MSI | 75 | 8 min |
| l3m3 | Gastos fijos vs variables | Fixed vs variable expenses | 75 | 6 min |
| l3m4 | Apoyos a familia: planear, no improvisar ★ | Family financial support as a planned expense | 80 | 7 min |
| l3m5 | Obligaciones fiscales del revendedor ★ | SAT / RESICO tax obligations for resellers | 80 | 8 min |

### Layer 4 — Escenarios e Inversión / Scenarios & Investing

| ID | Spanish Title | English Summary | XP | Time |
|----|--------------|-----------------|-----|------|
| l4m1 | ¿Qué harías tú? Parte 1 | Real-life money decisions, Part 1 | 85 | 10 min |
| l4m2 | ¿Qué harías tú? Parte 2 | Real-life money decisions, Part 2 | 90 | 10 min |
| l4m3 | Primeros pasos para invertir en México ★ | First steps investing in Mexico | 90 | 10 min |

### Layer 5 — Reflexión / Reflection

| ID | Spanish Title | English Summary | XP | Time |
|----|--------------|-----------------|-----|------|
| l5m1 | Revisión mensual | Monthly check-in (6 questions) | 65 | 6 min |
| l5m2 | Revisión trimestral ★ | Quarterly deep review (7 questions) | 70 | 8 min |

★ = ES-exclusive module with no v1.3 equivalent

---

## ES-Exclusive Modules — Detailed Notes

### l3m4 — Family Support: Plan It, Don't Wing It
This module addresses a reality common in Guadalajara: regular financial support sent to family members. The module reframes this not as an "extra" expense but as a real recurring commitment that belongs in the base budget. It covers: calculating a 6-month average, placing it in the budget as a fixed line item alongside rent, and how to communicate honestly when a difficult month means sending less. Tone is explicitly respectful — supporting family is treated as a value, not a problem to solve.

### l3m5 — Tax Obligations for Resellers
Covers: what the SAT (Mexico's IRS equivalent) requires, RFC registration, the RESICO simplified tax regime (1–2.5% annual rate, monthly declarations, up to $3.5M MXN/year), automatic withholding by MercadoLibre, how to credit withheld amounts against SAT declarations, basic record-keeping, and red flags that indicate you have obligations you may not be meeting. Explicit disclaimer: informational only, not tax advice — always consult an accountant. Links to sat.gob.mx.

### l4m3 — First Steps Investing in Mexico
Three accessible options from Guadalajara: **CETES Directo** (government bonds, near-zero risk, from $100 MXN, ~10% annual at current Banxico rate, signup at cetesdirecto.com); **Nu Inversiones** (daily interest on available balance, instant SPEI liquidity, ideal for emergency fund); **GBM+** (low-cost ETFs, next step after building foundation). Includes investment fraud red flags (common in Mexico): guaranteed returns over 5%/month, pressure to decide quickly, no CNBV registration, MLM-style recruitment model, deposits to personal accounts. Prerequisite framing: emergency fund first, high-cost debt first, then invest.

### l5m2 — Quarterly Review
Seven questions evaluated every three months: Did total debt decrease? Did the emergency fund grow? Did fixed expenses drop as a percentage of income? Have you started investing, even a little? Are family support payments in the budget? Are SAT obligations current? Name one financial habit you have now that you didn't three months ago.

---

## Technical Reference

### Key Differences from v1.3

| Feature | v1.3 | ES v1.0 |
|---------|------|---------|
| Language | English | Spanish (es-MX) |
| Currency | USD | MXN |
| localStorage key | `moneymind_v1_3` | `moneymind_es_v1` |
| Module count | 13 | 16 |
| Exclusive modules | — | l3m4, l3m5, l4m3, l5m2 |
| Debt calculator input | APR (annual %) | Monthly rate % (as shown by BBVA) |
| Emergency fund goal | $500 USD | $5,000 MXN |
| Income context | Gig delivery | Product reselling |
| Bank references | Generic / Ally | BBVA specifically |
| Family support | Not addressed | Core module (l3m4) |
| Tax obligations | Not addressed | Core module (l3m5) |
| Investing | Not addressed | Core module (l4m3) |
| Badges | 12 | 13 |
| Tips | 10 (English) | 10 (Spanish, MXN-adapted) |

### Calculators

**l1m3 Budget Calculator** (`calcBudget`)
- IDs: `bc-nomina`, `bc-reventa`, `bc-renta`, `bc-tel`, `bc-seguros`, `bc-deuda`, `bc-comida`, `bc-gas`, `bc-salidas`, `bc-familia`, `bc-subs`, `bc-varios`
- Live update on input. Result box: green (surplus), yellow (break-even), red (deficit). Advice text adapts to result.

**l2m1 Debt Payoff** (`calcDebt`)
- IDs: `calc-balance`, `calc-apr` (monthly %, e.g. 3.5), `calc-payment`
- Outputs: months to payoff, total interest, total paid. Uses `toLocaleString('es-MX')` for MXN formatting.

**l2m2 Income Buffer** (`calcBuffer`)
- IDs: `calc-fixed`, `calc-slow`, `calc-avg`
- Outputs: recommended buffer amount, contextual note based on whether slow month covers expenses.

**l2m3 Housing Cost** (`calcHousing`)
- IDs: `hc-renta`, `hc-luz`, `hc-internet`, `hc-gas`, `hc-agua`, `hc-hogar`
- Outputs: total monthly housing cost, per-person 50/50 split, rent as % of total.

### Storage
All data stored in `localStorage` under key `moneymind_es_v1`. Schema is identical to v1.3 (`userName`, `completedModules`, `xp`, `streak`, `lastActivity`). No server-side storage. No conflicts with v1.3 instances (different key).

### Fonts & Assets
- **Nunito** (body text) — Google Fonts
- **Lora** (section headings) — Google Fonts
- No external images, icons, or CDN dependencies beyond fonts
- All CSS custom properties (variables) defined in `:root`

### No-Build Architecture
Single HTML file. No build step, no npm, no bundler. Open in any browser. Deploy by uploading the `.html` file to any static host (GitHub Pages, Netlify, Vercel, S3).

---

## Build History

| Step | Content | Status |
|------|---------|--------|
| Step 1 | Spanish UI shell (fork of v1.3, all UI strings translated) | ✅ |
| Step 2 | l1m1 + l1m2 module content in Spanish with MXN amounts | ✅ |
| Step 3 | l1m3 + l1m4 + budget calculator with "Apoyos a familia" line | ✅ |
| Step 4 | Layers 2–5 complete, all 3 ES-exclusive modules, all JS data objects translated | ✅ |
| Step 5 | README ES + README EN | ✅ |

---

## Future Version Ideas

- **v1.1** — Dark mode
- **v1.2** — Export budget summary as shareable image
- **v2.0** — Payroll & benefits modules (IMSS, INFONAVIT, SAR), severance calculator
- **v2.1** — Resale business module: margins, working capital, scaling from side hustle to primary income

---

© 2026 Burle Warren · All Rights Reserved · MoneyMind ES v1.0
