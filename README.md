# 💧 AquaGuard
## Smart Water Conservation & Overflow Prevention Simulator

> **Sense Water. Predict Risk. Prevent Waste. Save Every Drop.**

AquaGuard is a browser-based simulation of an intelligent water-level monitoring and overflow prevention system.

The project demonstrates how sensor-based monitoring, decision logic, risk classification, predictive analysis and preventive actions can work together to reduce avoidable water wastage.

🚀 Developed as a **24-Hour National Level Hackathon MVP**.

---

## 🌍 Problem

Water tanks in homes, educational institutions, hostels, offices and other buildings can overflow when rising water levels are not monitored in time.

This can result in:

- 💧 Avoidable water wastage
- ⚡ Unnecessary energy consumption associated with pumping
- 🌱 Poor resource management
- 💰 Increased operational costs

AquaGuard demonstrates a technology-assisted approach to detecting rising water levels and providing timely preventive action.

---

# 💡 Our Solution

AquaGuard simulates an IoT-enabled water management system.

The simulator follows:

**Water Level → Sensor Reading → Decision Logic → Risk Analysis → Prediction → Alert → Preventive Action**

The current version is completely browser-based and does not require physical hardware.

---

# ⚙️ How AquaGuard Works

### 1. Water-Level Input

The user adjusts the simulated water level using an interactive slider or predefined scenarios.

### 2. Ultrasonic Sensor Simulation

The system converts the simulated water level into a corresponding sensor-to-water distance.

The prototype assumes a configurable tank height of 20 cm.

### 3. Risk Classification

The system classifies the current water level into four categories:

| Water Level | Status |
|-------------|--------|
| 0–59% | 🟢 NORMAL |
| 60–79% | 🟡 MEDIUM |
| 80–89% | 🟠 HIGH |
| 90–100% | 🔴 CRITICAL |

### 4. Overflow Prediction

AquaGuard estimates the time required for the simulated tank to reach the critical threshold based on a hypothetical water-level rise rate.

### 5. Smart Alerts

The system generates appropriate warnings when the simulated water level becomes high or critical.

### 6. Preventive Pump Control

The simulator can demonstrate a pump cutoff action.

An optional **Auto Protection** mode can simulate automatic pump shutdown when the level reaches the critical threshold.

---

# 🧠 System Architecture

```text
                 INPUT
                   │
                   ▼
        ┌─────────────────────┐
        │ Simulated Water     │
        │ Level                │
        └──────────┬──────────┘
                   │
                   ▼
        ┌─────────────────────┐
        │ Ultrasonic Sensor   │
        │ Simulation          │
        └──────────┬──────────┘
                   │
                   ▼
        ┌─────────────────────┐
        │ Water Level         │
        │ Calculation         │
        └──────────┬──────────┘
                   │
                   ▼
        ┌─────────────────────┐
        │ Risk Classification │
        └──────────┬──────────┘
                   │
                   ▼
        ┌─────────────────────┐
        │ Overflow Prediction │
        └──────────┬──────────┘
                   │
          ┌────────┴────────┐
          ▼                 ▼
       ALERT            PUMP ACTION
