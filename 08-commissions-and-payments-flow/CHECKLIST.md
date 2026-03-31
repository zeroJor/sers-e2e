# Commissions and payments — provider app + web panel

**Goal:** Provider accrues commission(s), views commissions in app, submits payment proof or uses payment URL flow; admin **Payments** approves or rejects; notifications/emails if applicable.

## Preconditions

- [ ] Data: at least one commission period or order pipeline that generates commission (may depend on schedule or seed data).
- [ ] Provider login with commissions visible in test env.
- [ ] Admin access to **Commissions** and **Payments**.
- [ ] Environment: `API __________` | `Web panel __________` | `Provider app build __________`

## Flow

### Provider app

- [ ] Open commissions/history; locate expected commission line items.
- [ ] Open payment flow: payment URL, upload receipt, or both—per current UI.
- [ ] Complete submission; capture reference.

### Web panel

- [ ] **Payments**: find pending payment; open detail.
- [ ] **Approve** path: mark approved; confirm provider-side status updates after refresh (or next sync).
- [ ] (Separate run) **Reject** path: reject with reason; provider sees updated state.

### Optional: provider portal

- [ ] If using token links (`/provider-portal/...`), verify account statement and receipt upload from browser.

## Result

| Outcome | Notes |
|---------|--------|
| Pass / Fail / Blocked | |

**Tester:** ______________ **Date:** ______________
