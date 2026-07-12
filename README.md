# EdgePulse
AI-Powered Edge Digital Twin for Semiconductor Manufacturing

Project Overview
Semiconductor manufacturing faces costly downtime.
Traditional SPC/APC workflows depend on cloud communication.
EdgePulse moves AI inference to the edge using LangGraph and Qualcomm AI Hub.
Human operators remain in control through a Human-in-the-Loop workflow.

Problem Statement
Modern manufacturing is rapidly transitioning to hybrid cloud architectures to maintain global
visibility and evaluate Overall Equipment Effectiveness (DEE). However, this creates a major
bottleneck: network latency. In high-speed, precision manufacturing, relying on centralized cloud
infrastructure for anomaly detection and process tracking introduces significant processing
delays. A delayed alarm by even a few seconds can result in catastrophic equipment damage
line downtime, or defective product batches before an intervention can happen
Compounding this issue, current factory floors utilize siloed, disconnected tools: Statistical
Process Control (SPC) metrics, Advanced Process Control (APC) data, and legacy
Manufacturing Execution Systems (MES). When a process anomaly occurs, these platforms
cannot seamlessly cross-reference historical data or manuals locally, rendering operators
incapable of fast, automated triage.
Key points indicate
Process variations occur across Lithography, Etching, CVD, CMP, and Inspection.
Cloud-based analysis introduces latency.
Delayed corrective actions reduce yield and increase downtime.

Proposed Solution
Agentic Edge Ecosystem
To bridge this gap, we are building a fully localized, Agentic Edge Ecosystem that integrates
hardware and multi-agent Al to achieve immediate anomaly detection and cross-system
orchestration entirely on the edge
Instead of waiting for a round-trip to the cloud, the solution acts as a real-time intelligent brain
on the factory floor. The core architecture uses specialized software agents to query local
knowledge databases, instantly validate alarms against historical logs, and compute precise
machine corrections
To maintain operational security, the ecosystem operates via a Human-in-the-Loop (HITL)
setup. A fail-safe mechanism routes critical machine data directly to an operator interface. If a
supervisor is away from the physical machine terminal, the system automatically escalates the
warning, pushing rich-text alert notifications containing reasoning and an "Approve Execution"
button to mobile phones over local networks to ensure critical oversight is never missed

System Architecture
Semiconductor Manufacturing

Lithography
      │
Etching
      │
CVD
      │
CMP
      │
Inspection
      │
────────────────────────────
Digital Twin
(10,000 Dummy Dataset)
────────────────────────────
      │
Physics Engine
      │
FastAPI Backend
      │
LangGraph Agent Orchestration
      │
────────────────────────────────────
Sensor Agent
SPC Agent
Knowledge (RAG) Agent
History Agent
Prediction Agent
Explanation Agent
Adjustment Agent
Recommendation Agent
────────────────────────────────────
      │
Qualcomm AI Hub Models
      │
APC Dashboard (React + Vite)
      │
Android HITL Application
      │
Operator Approval
      │
Arduino UNO Q
(Thermo + Knob + Buzzer)
      │
Recipe Recommendation

Technology Stack

Layer	Technology
Digital Twin	Python
Backend	FastAPI
AI Workflow	LangGraph
LLM	Qualcomm AI Hub
ML	XGBoost / SHAP
Frontend	React + Vite
Mobile	Android Studio
Hardware	Arduino UNO Q
Dataset	10,000 simulated records

Multi-Agent Workflow

Sensor Agent

SPC Agent

Knowledge (RAG) Agent

History Agent

Prediction Agent

Explanation Agent

Adjustment Agent

Recommendation Agent

Notification Agent

Digital Twin
Explain:

Recipe Manager

Physics Engine

Virtual Sensors

Equipment Health

Fault Injection

JSON Streaming

Qualcomm AI Hub Integration
-oss is used

APC Dashboard


Android Human-in-the-Loop


Arduino Prototype


Demo Workflow
Wafer
↓

Lithography

↓

Etching

↓

CVD

↓

Digital Twin

↓

Physics Engine

↓

FastAPI

↓

LangGraph Agents

↓

Qualcomm AI Hub

↓

Dashboard

↓

Android

↓

Human Approval

↓

Arduino Validation

↓

Recipe Recommendation

14. Installation

git clone https://github.com/yourusername/EdgePulse-AI.git
cd EdgePulse-AI

pip install -r requirements.txt

cd frontend
npm install
npm run dev

uvicorn backend.app:app --reload

15. Future Scope

Integration with real semiconductor equipment

OPC-UA/SECS-GEM connectivity

Real-time predictive maintenance

Federated learning across fabs

Multi-fab orchestration
