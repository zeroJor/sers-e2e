# Cross-app order fulfillment — user + provider + web panel

**Goal:** Single thread: **customer** places an order; **provider** receives it and advances through the full operational pipeline (accept/reject, sample collection, transit, delivery, result upload, etc.—per your product statuses); **customer** sees status and results; **web panel** shows the same order for operations/audit.

Coordinate two testers or two devices if needed.

## Preconditions

- [ ] User app: registered customer in coverage area.
- [ ] Provider app: account that is **available** for the selected service and receives the assignment (per matching rules).
- [ ] Web panel: **Orders** access.
- [ ] Environment: `API __________` | `Web panel __________` | `User app build __________` | `Provider app build __________`

## Flow

### User app

- [ ] Place order (minimal path from flow `04`).
- [ ] Note order id.

### Provider app

- [ ] See incoming order on dashboard/list.
- [ ] Accept order (or exercise reject + alternate path in a separate run).
- [ ] Execute each status transition in order until completion (collect samples → transit → delivery → upload results / confirm delivery—**use actual labels in the app**).
- [ ] Upload result files if required; handle errors (size/type) in a separate defect if needed.

### User app (again)

- [ ] Refresh order detail; statuses match provider actions within acceptable delay.
- [ ] Obtain results when marked complete.

### Web panel

- [ ] Same order visible; status history consistent with apps.
- [ ] Download results or view detail if permitted for admin role.

## Result

| Outcome | Notes |
|---------|--------|
| Pass / Fail / Blocked | |

**Tester:** ______________ **Date:** ______________
