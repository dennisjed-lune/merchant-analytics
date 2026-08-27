# Lune Pulse — Merchant Analytics

Per-brand merchant analytics dashboard for Lune Pulse (merchant-funded cashback campaigns).

`Pulse Analytics.dc.html` is fully self-contained (design-system tokens, fonts, runtime, and assets are inlined). Open it directly in a browser, or serve the folder with any static server.

## What it shows

- One analytics page per brand account, with a Slack-style brand switcher (Nero Coffee / Nero Market / Nero Bakehouse) in the sidebar.
- KPI grid (3x3): Campaign ROI (GMV / cashback allocated), unique customers, GMV driven, cashback allocated (paid/held split), tracked transactions, transactions settled, budget used, avg transaction value, CAC.
- Cashback and spend over time (Day/Week/Month), channel filter (All / In-store / Online) that adapts per brand.
- Engagement funnel in unique customers: audience reached, viewed, activated, transacted, settled transactions, settled.
- Campaign performance table: each campaign runs with a single bank partner (1:1), with GMV, tracked transactions, cashback, ROI, and budget pacing per campaign.
- Rejection reasons recorded by the cashback engine, transaction log, and an ROI definition panel.

## Data

All figures are synthetic but reconciled by construction: channel slices sum to all-channels totals, campaigns sum to brand totals, paid + held = allocated, and the day series sums to its week. Ground truth lives in the `brands()` function inside the `text/x-dc` script block; change data there only.

Imported from the "Pulse Analytics demo UX" claude.ai/design project and iterated locally.
