# ◊ FallMortgagePractice

**Sovereign firm-side accounting for UK FCA-regulated mortgage broker practices.** Single HTML file. All data stays on device. Prime 881.

Part of the **mortgage-firm bundle**: [fallmortgage](https://github.com/sjgant80-hub/fallmortgage) (859) · [fallmortgageonboard](https://github.com/sjgant80-hub/fallmortgageonboard) (863) · [fallmortgagepaper](https://github.com/sjgant80-hub/fallmortgagepaper) (877) · **fallmortgagepractice** (881).

Live: <https://sjgant80-hub.github.io/fallmortgagepractice/>

---

## For the end user · the 30-second pitch

You're running a mortgage broker firm. Procuration fees come in from lenders, broker fees from clients, protection commissions from insurers — and clawbacks go back out when clients redeem early. FallMortgagePractice tracks all of it in one HTML file: pipeline, per-adviser P&L, firm P&L, clawback exposure, compliance obligations, and expenses.

### 13 tabs

| Tab | What it does |
|---|---|
| Dashboard | KPIs: pipeline value, revenue by stream, net profit, clawback exposure |
| Pipeline | Case funnel (lead → DIP → applied → offered → exchanged → completed) |
| Procuration | Lender proc fee ledger with auto-calc from loan × rate |
| Broker Fees | Client fee ledger (fixed/percentage/hybrid, trigger point) |
| Protection | Life/CI/IP commission ledger |
| Clawback | Clawback events + cases still in clawback window |
| Schedules | Fee schedule templates for standardizing client charges |
| Clients | Client list with per-client revenue |
| Advisers | Per-adviser P&L with case counts |
| Firm P&L | Full revenue vs costs breakdown including PI, FCA levy, network |
| Expenses | Categorized expense ledger |
| Compliance | PI minimums, FCA fees, CPD, record retention, key rules |
| Q&A | T0 offline rules + T3 BYOK for mortgage broker practice questions |

### Key features

- **Procuration fee calculator**: enter loan amount + rate, fee auto-calculates
- **Clawback tracking**: cases in window with expiry dates and at-risk exposure
- **Network levy**: AR firms can set network % to see true net revenue
- **Command palette**: Ctrl+K to ask regulatory questions inline
- **Demo data**: 6 cases across pipeline stages, 2 advisers, protection, expenses

### Audit chain (P3)

Every data change appends a SHA-256 chained entry. Export for compliance records.

### Cross-tool mesh

BroadcastChannel `fall-mortgage` + `fall-signal`. Syncs clients, advisers, firm, and cases from sibling tools.

---

## For the developer · architecture

- **Single HTML** · ~65KB · zero runtime dependencies
- **IndexedDB** (`fallmortgagepractice-v1`) · 12 object stores
- **BroadcastChannel** · `fall-mortgage` + `fall-signal`
- **13 tab views** · all rendered client-side
- **T0** · 10 hard-coded UK mortgage broker rules · zero network
- **T3** · BYOK Anthropic · falls back if T0 misses
- **Command palette** · Ctrl+K · same T0/T3 cascade

### 14-pt sovereign gate

Single HTML · <400KB · Sovereign · IDB primary · KONOMI shim · fall-signal mesh · PWA manifest · Mobile responsive · T0 offline · Two-audience README · MIT · .nojekyll · Demo data · Audit chain

---

## Licence

MIT · Simon Gant · part of the [sjgant80-hub](https://github.com/sjgant80-hub) sovereign estate · prime 881 · ◊·κ=1.
