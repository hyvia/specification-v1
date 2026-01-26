# Mobile Application Specification – Player App (Flutter)

## Table of Contents
1. Overview
2. Components
   - Authentication & User Management
   - Wearable Device SDK Integration
   - Data Upload & API Communication
   - Dashboard
   - Profile & Settings
   - Notifications
3. Considerations
4. Implementation Estimation (Solo Flutter Developer)
5. Abstract Data Flow Diagram

---

## 1. Overview

The player mobile application is designed to capture, upload, and display player biometrics from wearable devices in real-time or near real-time. The app also provides a lightweight dashboard, profile management, and notifications. It communicates with the backend (AppSync/GraphQL API) for reading/writing data.

**Key goals:**
- Seamless data capture from wearables
- Efficient data upload to backend
- Lightweight dashboard for player insights
- Profile management and app settings
- Notifications for alerts and important events

---

## 2. Components

### 2.1 Authentication & User Management
- **Purpose:** Authenticate players and secure access to their data.
- **Implementation:** AWS Cognito (user pools)
- **Considerations:**
  - Multi-device login support
  - Secure token storage
  - Session refresh and expiration handling
- **Spec wording:**
> “The application uses a managed authentication system to securely log in players and control access to biometric data.”

---

### 2.2 Wearable Device SDK Integration
- **Purpose:** Capture biometric data from wearable devices.
- **Implementation:** Use manufacturer-provided Flutter SDK
- **Considerations:**
  - High-frequency data capture (e.g., every 1 min for HR, HRV)
  - Background operation to capture data continuously
  - SDK error handling and reconnection logic
  - Data validation (range checks, timestamp checks)
- **Spec wording:**
> “The app integrates with wearable SDKs to capture biometrics reliably and continuously, handling disconnections or errors gracefully.”

---

### 2.3 Data Upload & API Communication
- **Purpose:** Send captured data to backend for storage and analysis.
- **Implementation:**
  - GraphQL (AppSync) for queries and mutations
  - Batch or periodic upload of wearable data to optimize performance
- **Considerations:**
  - Offline caching if no network connectivity
  - Retry mechanism for failed uploads
  - Minimal impact on battery life
- **Spec wording:**
> “Captured data is periodically uploaded to the backend API with batching and retry mechanisms to ensure reliability and performance.”

---

### 2.4 Dashboard
- **Purpose:** Display lightweight player metrics and trends.
- **Components:**
  - Home screen shows top metrics (e.g., readiness, fatigue, HR trends)
  - Simple historical view (last N days)
- **Considerations:**
  - Pulls precomputed metrics from AppSync API (no heavy computation on mobile)
  - Uses role-specific data (player sees only their own metrics)
  - Offline caching for viewing without connectivity
- **Spec wording:**
> “The dashboard provides a concise view of player metrics using precomputed data from the backend for fast rendering and low resource usage.”

---

### 2.5 Profile & Settings
- **Purpose:** Manage player profile and app options.
- **Components:**
  - Update personal information (name, contact, etc.)
  - Adjust data collection settings (frequency, sensors enabled/disabled)
- **Considerations:**
  - Changes reflected in backend via API
  - Validation of inputs
- **Spec wording:**
> “The profile and settings section allows the player to manage personal information and app preferences, with all changes synchronized to the backend.”

---

### 2.6 Notifications
- **Purpose:** Alert players to important events or warnings.
- **Components:**
  - Local push notifications for thresholds (e.g., abnormal HR, alerts)
  - Optional guidance or reminders (hydration, recovery)
- **Considerations:**
  - Configurable thresholds for notifications
  - Background processing for monitoring alerts
  - Ensure notifications are not overly frequent to avoid fatigue
- **Spec wording:**
> “The application provides notifications for critical biometric events or alerts, configured based on thresholds and player preferences.”

---

## 3. Considerations
1. **Sleep / physiological events detection:**
   - Could be computed on-device (e.g., HR drop indicates sleep)
   - Could trigger a local or backend event for further processing
2. **Battery and performance:**
   - Continuous data capture must balance accuracy with power consumption
3. **Offline mode:**
   - Ensure data can be cached and uploaded later if offline
4. **SDK reliability:**
   - Handle device disconnections and retries
5. **Security:**
   - Store tokens securely
   - Encrypt sensitive data in transit and at rest

---

## 4. Implementation Estimation (Solo Flutter Developer)

| Task | Estimated Effort |
|------|----------------|
| Cognito authentication integration | 1 week |
| Wearable SDK integration | 2–3 weeks |
| Data upload & API communication | 1–2 weeks |
| Dashboard implementation | 1 weeks |
| Profile & settings implementation | 1 week |
| Notifications & alert system | 1 week |
| Testing & deployment | 1–2 weeks |

**Total:** ~6–10 weeks (assuming experienced Flutter developer)

> Notes: Includes time for SDK integration, offline support, and ensuring battery-friendly operations. SDK integration will is already being investigated.

---

## 5. Abstract Data Flow Diagram
```
Wearable Device
       ↓
Mobile App (Flutter SDK)
       ↓
Data Upload (GraphQL / AppSync API)
       ↓
Backend Raw Data Storage & Computation
       ↓
Derived Metrics → Dashboard (Player App)
       ↓
Notifications (if thresholds exceeded)
```

