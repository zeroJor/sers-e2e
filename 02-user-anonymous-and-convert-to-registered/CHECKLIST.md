# Anonymous (guest) user → convert to registered — full flow

**Goal:** Guest browses/uses the app with an anonymous token, then completes **convert to registered** without losing the intended cart/session behavior (per app rules).

## Preconditions

- [ ] App supports guest entry (anonymous registration) for this environment.
- [ ] Test email/phone for conversion not already registered.
- [ ] Environment: `API __________` | `Web panel __________` | `User app build __________`

## Flow

### User app — anonymous

- [ ] Start as guest / continue without full registration (per initial screen).
- [ ] Add item(s) to cart or perform allowed guest actions.
- [ ] Note any identifiers shown (if any) for support correlation.

### User app — convert

- [ ] Trigger **convert to registered** (or equivalent) from settings/cart flow.
- [ ] Complete personal data, password, OTP.
- [ ] After success: previously relevant cart/state behaves as specified (retained or cleared per spec).

### Web panel

- [ ] Find the user under **Customers** as a registered customer (not only anonymous if both appear).
- [ ] Confirm profile matches conversion data.

## Result

| Outcome | Notes |
|---------|--------|
| Pass / Fail / Blocked | |

**Tester:** ______________ **Date:** ______________
