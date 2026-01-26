# Backend Architecture Specification – Football Club Wearables Platform

## Table of Contents
1. Overview
2. Components
   - Authentication & User Management
   - Data Ingestion Layer
   - Raw Data Storage Layer
   - Analytics / Computation Layer
   - Derived Metrics Storage Layer
   - AI Prediction Layer
   - API Layer
   - Background Scheduling / Event Triggering
3. Architectural Considerations
4. Implementation Estimation (Solo Developer)
5. Abstract Data Flow Diagram

---

## 1. Overview

The backend system supports ingestion, storage, processing, and delivery of biometric data from player wearables and sweat patch measurements. It provides both current state metrics and predictive insights for coaches. The architecture must be scalable, resilient, and performant while separating concerns between raw data storage, computation, and dashboard delivery.

**Backend Architecture Layers:**
1. Authentication & User Management
2. Data Ingestion Layer
3. Raw Data Storage Layer
4. Analytics / Computation Layer
5. Derived Metrics Storage Layer
6. AI Prediction Layer
7. API Layer (AppSync)
8. Background Scheduling / Event Triggering

---

## 2. Components

### 2.1 Authentication & User Management
- **Purpose:** Authenticate players and coaches, manage roles, and secure access to data.
- **Implementation:** AWS Cognito (user pools and identity management).
- **Roles:**
  - Players: Upload wearable data, view own metrics
  - Coaches: View all players, trigger predictions, configure events
- **Considerations:**
  - Multi-device login
  - Secure communication from devices
  - Token refresh & session management
- **Spec wording:**
> “User authentication and authorization is handled through a managed identity system supporting role-based access. Different roles provide different visibility and permissions to system data.”

### 2.2 Data Ingestion Layer
- **Purpose:** Receive data from mobile app (wearables) and coach laptop/web app (sweat patch readings).
- **Components:**
  - Event-based ingestion functions (Lambdas)
  - Message/event bus to decouple ingestion from processing
- **Considerations:**
  - High-frequency wearable data batching
  - Data validation at ingestion (timestamps, value ranges)
- **Spec wording:**
> “The ingestion layer accepts high-frequency and discrete biometric measurements, validates the input, and queues them for processing to maintain performance and scalability.”

### 2.3 Raw Data Storage Layer
- **Purpose:** Immutable storage of all incoming measurements.
- **Implementation:** Scalable time-series optimized database (e.g., DynamoDB)
- **Tables:**
  - WearableReadings: HR, HRV, SpO2, RR, BP, GSR, timestamps
  - SweatMeasurements: lactate, cortisol, timestamps
- **Considerations:**
  - Raw data must never be modified
  - Supports queries for recent N weeks per player
  - Enables auditing and historical analysis
- **Spec wording:**
> “All raw biometric data is stored in an immutable, time-series optimized database layer to support historical queries, algorithmic computation, and auditing.”

### 2.4 Analytics / Computation Layer
- **Purpose:** Transform raw data into derived, dashboard-ready metrics.
- **Components:**
  - Event-driven and/or scheduled processing jobs
  - Compute derived metrics: Fatigue, Readiness, Stress, Recovery
- **Processing Approach:**
  - Aggregates historical and recent measurements
  - Deterministic/statistical algorithms (no AI) for current state
  - Outputs precomputed metrics to dashboard-ready storage
- **Considerations:**
  - Event triggers: End of training, sweat patch upload, physiological events (sleep/wake)
  - Continuous vs batch processing
  - Incremental vs full historical recomputation
- **Spec wording:**
> “The computation layer aggregates historical and current biometric data to derive meaningful player metrics for the dashboard. Computation is triggered by discrete events or detected physiological patterns.”

### 2.5 Derived Metrics Storage Layer
- **Purpose:** Store precomputed metrics for fast dashboard consumption.
- **Components:**
  - Separate tables for dashboard metrics (e.g., PlayerState table: readiness, fatigue, stress, flags)
- **Considerations:**
  - Ensures low-latency reads
  - Algorithm updates do not affect raw data
- **Spec wording:**
> “Derived metrics are stored in a separate, dashboard-optimized data layer to enable fast and consistent access by client applications.”

### 2.6 AI Prediction Layer
- **Purpose:** Provide predictive insights for upcoming matches or post-microcycle analysis.
- **Components:**
  - ML model(s) trained on historical player data
  - Runs on-demand (dashboard button) or scheduled (weekly, pre-match)
  - Output stored in separate prediction table
- **Considerations:**
  - AI only predicts future performance
  - Computationally expensive, schedule for cost efficiency
  - Supports manual triggering by coach
- **Spec wording:**
> “The AI layer analyzes historical data to predict player performance for future matches or training cycles. It is triggered either automatically on schedule or manually by the coach, and its outputs are stored separately from current metrics.”

### 2.7 API Layer
- **Purpose:** Provide GraphQL API for mobile and web applications.
- **Components:**
  - Unified API (AppSync) serving both players and coaches
  - Role-based field access: Players → own metrics, Coaches → all players + predictions
  - Queries/mutations: Upload biometric data, Retrieve metrics, Trigger AI predictions
- **Considerations:**
  - Keep client logic thin
  - Supports real-time updates (optional subscriptions)
- **Spec wording:**
> “A unified API layer provides access to both current and predicted player metrics, with role-based authorization ensuring appropriate data visibility.”

### 2.8 Background Scheduling / Event Triggering
- **Purpose:** Determine when analytics and AI predictions run.
- **Triggers:**
  - Discrete events: end of training, sweat patch upload
  - Continuous monitoring: detect physiological events (sleep/wake)
  - Scheduled: weekly microcycle, pre-match
- **Considerations:**
  - Continuous signals detected on device or backend
  - Batch processing reduces load
- **Spec wording:**
> “The system supports both event-driven and scheduled processing. Event-driven computations respond to user actions or detected physiological events, while scheduled jobs support regular aggregation and AI predictions. This ensures timely, scalable, and cost-efficient analytics.”

---

## 3. Architectural Considerations
1. Raw vs Derived Separation: Raw data immutable; derived metrics allow updates without impacting clients.
2. Scalability & Performance: High-frequency wearable data requires batching and decoupled processing.
3. Event-driven vs Continuous Processing: Events for discrete actions; continuous streams for physiological events.
4. AI Costs: Predictive computations scheduled or manual to control cost.
5. Dashboard Readability: Derived tables ensure low-latency reads.
6. Security & Access Control: Role-based API, secure transport from devices.

---

## 4. Implementation Estimation (Solo Developer)

| Task | Estimated Effort |
|------|----------------|
| Cognito setup & authentication | 1–2 weeks |
| AppSync API design | 1 week |
| Raw data ingestion layer | 2–3 weeks |
| Raw data storage | 1 week |
| Analytics / computation layer | 3–4 weeks |
| Derived metrics storage | 1–2 weeks |
| Event scheduling | 1–2 weeks |
| AI prediction layer | 3–4 weeks |
| Testing & deployment | 2–3 weeks |

**Total:** ~15–22 weeks

> Notes: Includes learning curve for AWS Cognito/AppSync and AI implementation.

---

## 5. Abstract Data Flow Diagram
```
Mobile App / Coach Laptop
        ↓
   Data Ingestion Layer (Lambda + Event Bus)
        ↓
      Raw Data Storage
        ↓
   Analytics / Computation Layer
        ↓
Derived Metrics Storage → Dashboard (mobile/web)
        ↓
      AI Prediction Layer
        ↓
Predicted Metrics Storage → Dashboard (mobile/web)
```

