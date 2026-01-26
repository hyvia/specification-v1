# Project Roadmap – Football Club Wearables Platform

This roadmap describes the phases for building the wearable platform, including player mobile app, coach dashboard, and backend architecture. Current and estimated phases are outlined below, including dependencies and estimated durations. Phase 3 includes links to detailed specifications.

---

## Phase 1 – Requirements & Algorithm Definition (Current Phase)

**Objective:** Define coach dashboard layout, user experience, and biomarker algorithms.

**Tasks:**

* Discuss dashboard design with coaches.
* Consult with medical team for biomarker algorithm definition.
* Determine player categorization metrics.
* Document specifications for backend, player app, and coach dashboard.

**Dependencies:** None

**Estimated Duration:** 1–2 months (team effort)

---

## Phase 2 – SDK Testing & Data Validation

**Objective:** Test all device SDKs and validate data accuracy.

**Tasks:**

* Test player wearable SDK integration in mobile app.
* Test coach team device SDK integration.
* Validate real device data (wearables, lactate, cortisol patches).
* Ensure communication with backend APIs.

**Dependencies:** Phase 1

**Estimated Duration:** 1 week (can extend to 2–3 weeks for thorough validation)

---

## Phase 3 – Core Implementation

**Objective:** Build the player app, coach device upload, backend architecture, and dashboards.

**Tasks:**

* Player mobile app: implement authentication, SDK integration, data upload.
* Coach dashboard: implement device data upload (lactate & cortisol) and basic analytics.
* Backend architecture: implement raw data ingestion, computation layer, derived metrics storage, AppSync API.
* Dashboard UI: player metrics and team comparison views.
* **Linking Specifications:**

  * [Backend Specification](./backend.md)
  * [Player Mobile App Specification](./player-app.md)
  * [Coach Dashboard Specification](./coach-app.md)

**Dependencies:** Phase 2

**Estimated Duration (Software Developer):** 20–24 weeks (solo developer handling all software)

---

## Phase 4 – Testing & Validation

**Objective:** Test complete system with players, coaches, and real devices.

**Tasks:**

* Validate algorithms for accuracy and consistency.
* Test data flow end-to-end (wearables → backend → dashboards).
* UI/UX testing for player app and coach dashboard.
* Iterative bug fixing and adjustments.
* Conduct stress testing for multiple players.

**Dependencies:** Phase 3

**Estimated Duration:** 1 month

---

## Overall Estimation for Software Development (Solo Developer)

* **Phase 3:** 20–24 weeks

**Total:** ~5–6 months for solo development

> Notes: Total project duration including all phases and team activities may extend up to 6–8 months. Phase 1 and 2 involve team members from medical and data analytics, Phase 3 is primarily software development work & Phase 4 involves team members and eary customers.
