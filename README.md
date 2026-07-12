# EdgePulse

> **AI-Powered Agentic Edge Digital Twin for Semiconductor Manufacturing**

An on-premise, multi-agent AI platform that reduces semiconductor manufacturing downtime through real-time anomaly detection, explainable AI, and Human-in-the-Loop decision making.

---

# Overview

Semiconductor manufacturing is one of the most precision-driven industries, where even a small variation in process parameters can lead to defective wafers, equipment downtime, and significant production losses.

Traditional manufacturing environments rely on **Statistical Process Control (SPC)**, **Advanced Process Control (APC)**, and **Manufacturing Execution Systems (MES)**. These systems often depend on cloud communication, introducing latency during anomaly detection and corrective actions.

**EdgePulse** brings intelligence directly to the factory floor by combining a **Digital Twin**, **LangGraph-based Multi-Agent AI**, **Qualcomm AI Hub (-oss)** optimized models, and a **Human-in-the-Loop (HITL)** workflow to enable localized, explainable, and real-time manufacturing decisions.

---

# Problem Statement

Modern semiconductor fabrication plants continuously monitor thousands of process parameters across manufacturing stages such as Lithography, Etching, CVD, CMP, and Inspection.

Although SPC, APC, and MES generate valuable operational data, these systems are often siloed and heavily dependent on centralized cloud infrastructure.

This introduces several challenges:

- Network latency delays anomaly detection.
- Corrective actions arrive after additional wafers have already been processed.
- SPC, APC, and MES data remain disconnected.
- Operators manually correlate alarms with historical logs and equipment manuals.
- Delayed intervention reduces yield and increases equipment downtime.

In high-volume semiconductor manufacturing, even a few seconds of delay can result in defective wafer batches, expensive equipment damage, and significant operational losses.

---

# Our Solution

EdgePulse introduces an **Agentic Edge Ecosystem** that performs intelligent manufacturing decisions entirely on-premise.

Instead of sending every event to the cloud, EdgePulse deploys specialized AI agents alongside the manufacturing process.

The platform:

- Simulates the complete manufacturing workflow using a Digital Twin.
- Continuously monitors process parameters.
- Detects anomalies in real time.
- Retrieves historical manufacturing knowledge using Retrieval-Augmented Generation (RAG).
- Predicts process outcomes using Machine Learning.
- Explains predictions using Explainable AI (SHAP).
- Generates optimized APC recipe recommendations using Large Language Models.
- Requests operator approval through a Human-in-the-Loop workflow before applying recipe adjustments.

By bringing intelligence directly to the edge, EdgePulse minimizes response time while maintaining operational safety, transparency, and operator control.

---

# Why EdgePulse?

| Traditional Manufacturing | EdgePulse |
|----------------------------|-----------|
| Cloud-dependent anomaly detection | Edge AI inference |
| Manual root cause analysis | AI-assisted SHAP explanations |
| Siloed SPC/APC/MES systems | Unified Agentic AI workflow |
| Delayed corrective actions | Real-time recommendations |
| Limited explainability | Explainable AI + RAG |
| High operator workload | Human-in-the-Loop automation |

---

# Key Features

- Digital Twin of Semiconductor Manufacturing
- LangGraph Multi-Agent AI Workflow
- Qualcomm AI Hub (-oss) Optimized Models
- Retrieval-Augmented Generation (RAG)
- Explainable AI using SHAP
- Machine Learning Prediction Models
- React-based APC Dashboard
- Android Human-in-the-Loop Application
- Arduino UNO Q Edge Validation Prototype
- FastAPI Backend with Real-Time APIs

---

# System Architecture

```text
                    Semiconductor Manufacturing

 Lithography → Etching → CVD → CMP → Inspection
        │
        ▼
 Digital Twin (10,000 Dummy Dataset)
        │
        ▼
 Physics Engine
(Process Simulation)
        │
        ▼
 FastAPI Backend
        │
        ▼
 LangGraph Multi-Agent Workflow
        │
 ┌──────┼───────────────┐
 │      │       │       │
 ▼      ▼       ▼       ▼
Sensor  SPC  Knowledge  History
Agent   Agent  (RAG)     Agent
        │
        ▼
Prediction Agent
        │
        ▼
Explanation Agent (SHAP)
        │
        ▼
Adjustment Agent (LLM)
        │
        ▼
Recommendation Agent
        │
        ▼
Qualcomm AI Hub (-oss)
        │
        ▼
React APC Dashboard
        │
        ▼
Android HITL Application
        │
        ▼
Operator Approval
        │
        ▼
Arduino UNO Q
(Thermo • Knob • Buzzer)
        │
        ▼
Recipe Recommendation
```

---

# Technology Stack

| Layer | Technology |
|--------|------------|
| Digital Twin | Python |
| Backend | FastAPI |
| Multi-Agent Workflow | LangGraph |
| AI Optimization | Qualcomm AI Hub (-oss) |
| Machine Learning | XGBoost |
| Explainable AI | SHAP |
| Knowledge Retrieval | RAG |
| Frontend | React + Vite |
| Mobile | Android Studio |
| Hardware | Arduino UNO Q |
| Dataset | 10,000 Simulated Manufacturing Records |

---

# Multi-Agent Workflow

### Sensor Agent
Collects real-time manufacturing parameters from the Digital Twin and edge devices.

### SPC Agent
Continuously monitors Statistical Process Control metrics and detects process deviations.

### Knowledge Agent (RAG)
Retrieves equipment manuals, SOPs, maintenance guides, and historical manufacturing knowledge.

### History Agent
Analyzes historical production logs and previous manufacturing runs to identify recurring patterns.

### Prediction Agent
Uses Machine Learning models to predict process quality, equipment behavior, and potential failures.

### Explanation Agent
Generates interpretable explanations using SHAP to justify every AI prediction.

### Adjustment Agent
Uses Large Language Models to recommend optimized APC recipe adjustments.

### Recommendation Agent
Combines outputs from all agents into a single actionable recommendation.

### Notification Agent
Sends alerts to the APC Dashboard and Android application for Human-in-the-Loop approval.

---

# Digital Twin

The Digital Twin simulates an end-to-end semiconductor manufacturing environment using more than **10,000 synthetic manufacturing records**.

It includes:

- Recipe Manager
- Physics Engine
- Virtual Sensors
- Equipment Health Monitoring
- Fault Injection Engine
- JSON Data Streaming

This enables realistic experimentation and validation without requiring physical semiconductor fabrication equipment.

---

# Qualcomm AI Hub Integration

EdgePulse leverages **Qualcomm AI Hub (-oss)** to optimize AI inference for low-latency edge deployment.

The optimized models accelerate:

- Machine Learning inference
- Explainable AI workflows
- Large Language Model reasoning
- On-device execution with minimal cloud dependency

---

# APC Dashboard

The React + Vite dashboard provides:

- Live Process Monitoring
- SPC Trend Analysis
- Equipment Health Visualization
- AI Recommendations
- SHAP Explainability
- Process Stability Indicators
- Historical Analytics
- Real-Time Alerts

---

# Human-in-the-Loop (HITL)

The Android application ensures operators remain in control of every critical manufacturing decision.

Features include:

- Instant anomaly notifications
- Root cause analysis
- Confidence score
- AI-generated recommendations
- Approve / Reject workflow
- Emergency escalation
- Live process monitoring

---

# Arduino Edge Validation

Arduino UNO Q serves as an edge validation prototype demonstrating real-time interaction with the AI ecosystem.

Hardware Components:

- Modulino Thermo → Simulated Chamber Temperature
- Modulino Knob → Process Parameter Adjustment
- Modulino Buzzer → Real-Time Alarm System

The Arduino prototype validates live parameter changes before deployment to industrial semiconductor equipment.

---

# Demo Workflow

```text
Wafer Processing
        │
        ▼
Lithography
        │
        ▼
Etching
        │
        ▼
CVD
        │
        ▼
CMP
        │
        ▼
Inspection
        │
        ▼
Digital Twin
        │
        ▼
Physics Engine
        │
        ▼
FastAPI Backend
        │
        ▼
LangGraph Multi-Agent AI
        │
        ▼
Qualcomm AI Hub (-oss)
        │
        ▼
React APC Dashboard
        │
        ▼
Android HITL
        │
        ▼
Operator Approval
        │
        ▼
Arduino UNO Q Validation
        │
        ▼
Optimized Recipe Recommendation
```

---

# Repository Structure

```text
EdgePulse/
│
├── backend/
├── frontend/
├── agents/
├── digital_twin/
├── qualcomm_ai_hub/
├── android/
├── arduino/
├── datasets/
├── docs/
├── assets/
├── scripts/
├── README.md
├── requirements.txt
└── LICENSE
```

---

# Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/EdgePulse.git

# Navigate into the project
cd EdgePulse

# Install Python dependencies
pip install -r requirements.txt

# Start Backend
uvicorn backend.app:app --reload

# Start Frontend
cd frontend
npm install
npm run dev
```

---

# Future Scope

- Integration with real semiconductor fabrication equipment
- SECS/GEM and OPC-UA industrial connectivity
- Predictive maintenance across manufacturing tools
- Federated learning across multiple semiconductor fabs
- Autonomous recipe optimization using Reinforcement Learning
- Multi-fab orchestration through distributed Edge AI
- Digital Twin synchronization with live production environments

---

# Team Vision

EdgePulse aims to transform semiconductor manufacturing by bringing **AI closer to the factory floor**. Through Digital Twins, Agentic AI, Edge Computing, Explainable AI, and Human-in-the-Loop decision making, we envision a future where manufacturing systems become more intelligent, transparent, resilient, and capable of minimizing downtime while maximizing productivity.

---
