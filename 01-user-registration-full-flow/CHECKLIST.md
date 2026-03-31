# User registration — full flow (user app + web panel)

**Goal:** Validate a new customer registration from the user app through to a state that can be confirmed in the Sers web panel (and mail/OTP behavior as designed).

## Preconditions

- [ ] Clean or dedicated test email/phone (not already registered).
- [ ] Web panel admin (or staff) credentials available.
- [ ] Environment: `API __________` | `Web panel __________` | `User app build __________`

## Flow

### User app

- [ ] Open app → start registration (personal data → password → OTP as applicable).
- [ ] Complete OTP/email verification.
- [ ] Land on home or success state; session persisted after restart.
- [ ] Optional: verify profile fields match what was entered.

### Web panel (sers-server)

- [ ] Log in to the web panel.
- [ ] Open **Customers** (or equivalent list) and locate the new user by email/phone/name.
- [ ] Confirm record fields and status match expectations (verified email, etc., per product rules).

### Backend / observability (if used by QA)

- [ ] OTP/email received within expected time; invalid OTP rejected.

## Result

| Outcome | Notes |
|---------|--------|
| Pass / Fail / Blocked | |

**Tester:** ______________ **Date:** ______________
