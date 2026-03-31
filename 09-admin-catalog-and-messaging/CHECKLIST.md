# Admin catalog, configuration, and messaging (web panel + user app smoke)

**Goal:** Staff maintains **categories**, **services**, and **system configuration**; sends **messaging** (broadcast or targeted) if applicable. Short **user app** pass confirms catalog changes surface to customers (not an isolated admin test).

**Note:** This flow is still “whole story” for operations: config changes → customer-visible behavior.

## Preconditions

- [ ] Admin web panel access (categories, services, system configuration, messaging).
- [ ] User app available for a quick verification browse.
- [ ] Environment: `API __________` | `Web panel __________` | `User app build __________`

## Flow

### Web panel

- [ ] **Categories**: create or edit a category; save.
- [ ] **Services**: create or edit a service linked to category; set price/duration fields per form.
- [ ] **System configuration**: update a safe test flag or value (document key changed).
- [ ] **Messaging**: search users, send a test message or notification (per UI); verify audit/log expectation.

### User app (smoke)

- [ ] Refresh or restart app; open services list.
- [ ] Confirm new/edited category or service appears as expected (or hidden per rules).

## Result

| Outcome | Notes |
|---------|--------|
| Pass / Fail / Blocked | |

**Tester:** ______________ **Date:** ______________
