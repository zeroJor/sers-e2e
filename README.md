# Sers — Manual end-to-end tests

Manual test packs for QA. Each folder is **one full flow** across the **user mobile app**, **provider mobile app**, and **Sers server web panel** (Laravel admin), plus API/backend behavior where it matters for validation.

**Out of scope:** marketing website / landing (`sers-landing`) and any site that is not the authenticated admin application served by `sers-server`.

## How to use

1. Pick a flow folder (numbered for a suggested order; dependencies are noted in each checklist).
2. Open `CHECKLIST.md` in that folder.
3. Execute steps in order. A single case may move between **User app → Provider app → Web panel** (or the reverse)—that is intentional.
4. Record pass/fail, build/version, environment, and notes in the checklist or your test tool.

## Conventions

| Column / section | Meaning |
|------------------|--------|
| **User app** | `sers-user` (customer) |
| **Provider app** | `sers-provider` |
| **Web panel** | Browser UI backed by `sers-server` (dashboard, orders, providers, commissions, etc.) |

## Folder index

| Folder | Flow summary |
|--------|----------------|
| `01-user-registration-full-flow` | New customer registers on the user app; verify data and behavior in the web panel where applicable. |
| `02-user-anonymous-and-convert-to-registered` | Guest/anonymous usage, then convert to a full account (still crosses app + server). |
| `03-user-login-and-password-recovery` | Login and password reset; includes email/OTP behavior and post-login access. |
| `04-user-ordering-journey-browse-to-results` | Browse services, cart, address, place order, track order, obtain results (user app + web panel checks as needed). |
| `05-provider-registration-full-flow` | Provider registers on the provider app; documents and record visible/verifiable via web panel. |
| `06-provider-onboarding-and-settings` | Post-login validation, profile, services/prices, hours, coverage—provider app with web panel cross-checks where useful. |
| `07-cross-app-order-fulfillment` | End-to-end: customer order → provider accepts and runs the full status pipeline → outcomes visible to user and in the web panel. |
| `08-commissions-and-payments-flow` | Provider commissions, payment upload/approval, admin payments—provider app + web panel. |
| `09-admin-catalog-and-messaging` | Categories, services, system configuration, admin messaging—supports releases; may combine with a short user-app smoke to confirm catalog surfacing. |

## Environments

Document the API base URL, web panel URL, app build numbers, and test accounts in each run (templates are in each `CHECKLIST.md`).
