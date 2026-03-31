# Provider onboarding and settings (provider app + web panel cross-checks)

**Goal:** After registration/login, provider passes any pre-home gates, configures profile: opening hours, coverage, minimum order, service prices/list, address. Confirm critical data appears consistently if mirrored in the web panel or in downstream orders.

## Preconditions

- [ ] Provider account approved/valid for login (per environment rules).
- [ ] Test services/prices data prepared if required.
- [ ] Environment: `API __________` | `Web panel __________` | `Provider app build __________`

## Flow

### Provider app

- [ ] Cold start: session restore or login works.
- [ ] Complete **pre-home** / validation screens if shown (profile completeness).
- [ ] Set **opening hours** (and working days if separate).
- [ ] Set **coverage** / service area if applicable.
- [ ] Set **minimum order amount** if applicable.
- [ ] Configure **services and prices** (add/remove services, price list).
- [ ] Confirm **address** / location still correct.

### Web panel (spot checks)

- [ ] Open provider record; align key fields with app (business rules).
- [ ] If orders exist: confirm provider configuration affects availability/pricing as expected (tie to flow `07` when possible).

## Result

| Outcome | Notes |
|---------|--------|
| Pass / Fail / Blocked | |

**Tester:** ______________ **Date:** ______________
