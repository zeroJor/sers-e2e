# User ordering journey — browse to results (user app + web panel)

**Goal:** One continuous customer journey: discover services, configure cart (date/time, details), set address, place order, follow status, and retrieve results. Web panel validates server-side order visibility and artifacts (e.g. results access rules).

## Preconditions

- [ ] Logged-in user (non-anonymous if orders require it).
- [ ] Service area / address that matches at least one provider in test data.
- [ ] Web panel access to **Orders** (and **Customers** if needed).
- [ ] Environment: `API __________` | `Web panel __________` | `User app build __________`

## Flow

### User app

- [ ] Browse categories/services; open service detail.
- [ ] Add to cart; open cart; adjust quantities if applicable.
- [ ] Complete address step (map/location as applicable).
- [ ] Complete date/time and any required patient/sample details.
- [ ] Submit order; receive confirmation with order id or reference.
- [ ] Open order list/detail; status progresses (may depend on provider—coordinate with flow `07` or use staging data).
- [ ] When results are available: download or open results per app (link, PDF, etc.).

### Web panel

- [ ] Find the same order under **Orders**; status and customer link match app.
- [ ] If policy allows: open/download results from admin side for audit (mirror of customer rules).

## Result

| Outcome | Notes |
|---------|--------|
| Pass / Fail / Blocked | |

**Tester:** ______________ **Date:** ______________
