# Provider registration — full flow (provider app + web panel)

**Goal:** New provider completes registration on the provider app (personal data, address, location, password, OTP, provider data including kind and regulatory file where required). Admin can see the provider and documents in the web panel.

## Preconditions

- [ ] Dedicated test email/phone for provider registration.
- [ ] Test COFEPRIS (or required) document file for upload.
- [ ] Web panel credentials with access to **Providers**.
- [ ] Environment: `API __________` | `Web panel __________` | `Provider app build __________`

## Flow

### Provider app

- [ ] From login, go to registration.
- [ ] Enter provider data (name, kind: lab / blood bank per feature flags, health officer, phone, email, document upload).
- [ ] Complete address and map/location steps.
- [ ] Set password; complete OTP.
- [ ] Reach post-auth screen (e.g. pre-home / validation) as per current product.

### Web panel

- [ ] Log in; open **Providers** list.
- [ ] Locate new provider by email/name.
- [ ] Open detail; verify fields match registration.
- [ ] Download or view **COFEPRIS document** route if applicable (`providers/{id}/cofepris-document` or UI equivalent).

## Result

| Outcome | Notes |
|---------|--------|
| Pass / Fail / Blocked | |

**Tester:** ______________ **Date:** ______________
