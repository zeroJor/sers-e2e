# User login and password recovery — full flow

**Goal:** Existing customer can log in; user who forgot password can reset via OTP/email and regain access. Web panel used only if you need to confirm account state or unlock edge cases.

## Preconditions

- [ ] Registered test user credentials (known password).
- [ ] Access to test email/SMS inbox for OTP.
- [ ] Environment: `API __________` | `Web panel __________` | `User app build __________`

## Flow

### User app — login

- [ ] Log out or use fresh install.
- [ ] Log in with valid credentials → lands in app home.
- [ ] Invalid password shows expected error; no session leak.

### User app — password recovery

- [ ] From login, start **forgot password** flow.
- [ ] Request OTP to email/phone; receive and enter OTP.
- [ ] Set new password; confirm policy validation (length/complexity).
- [ ] Log in with **new** password successfully.

### Web panel (optional cross-check)

- [ ] If troubleshooting: locate user in **Customers**; confirm `email_verified_at` / status per policy after reset.

## Result

| Outcome | Notes |
|---------|--------|
| Pass / Fail / Blocked | |

**Tester:** ______________ **Date:** ______________
