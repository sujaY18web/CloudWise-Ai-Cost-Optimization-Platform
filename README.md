# CloudWise AI — AI-Powered Cloud Cost Intelligence & Optimization Platform

[![Python 3.13](https://img.shields.io/badge/python-3.13-blue.svg)](https://www.python.org/downloads/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.115+-009688.svg)](https://fastapi.tiangolo.com)
[![React 19](https://img.shields.io/badge/React-19.2+-61DAFB.svg)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0+-3178C6.svg)](https://www.typescriptlang.org)
[![Tailwind CSS v4](https://img.shields.io/badge/TailwindCSS-4.0-38B2AC.svg)](https://tailwindcss.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **CloudWise AI** is an enterprise-grade, full-stack cloud cost intelligence and FinOps platform that empowers engineering leaders, DevOps, and FinOps teams to **observe, analyze, detect, predict, explain, optimize, simulate, prioritize, approve, and verify** cloud infrastructure spending.

---

## 🚀 Live Placement & CV Summary

> **Resume Bullet:**
> *"Engineered **CloudWise AI**, a production-grade FinOps platform combining FastAPI, React 19, and statistical ML to analyze AWS telemetry across 327 active resources. Implemented an algorithmic Knapsack budget solver, Holt-Winters seasonal forecasting with 80%/95% confidence intervals, an automated period-over-period variance engine ('Why Did My Bill Increase?'), time-travel counterfactual simulations, and a human-in-the-loop savings verification pipeline."*

---

## 🏛️ System Architecture

```
                                [ User / FinOps Team ]
                                           │
                     ┌─────────────────────┴─────────────────────┐
                     ▼                                           ▼
           [ Modern Web Interface ]                    [ Voice Query / Mic ]
       React 19 + TypeScript + Vite                   Web Speech API Recognition
       Tailwind CSS + Recharts + Lucide               SpeechSynthesis Spoken Audio
                     │                                           │
                     └─────────────────────┬─────────────────────┘
                                           ▼
                                [ FastAPI REST Backend ]
                                   (Python 3.13)
                                           │
           ┌───────────────────────────────┼───────────────────────────────┐
           ▼                               ▼                               ▼
  [ Analytics Engine ]             [ ML & Algorithms ]             [ AI Explanations ]
  • Multi-dim Aggregations         • Linear/Seasonal Forecast      • "Why Did Bill Increase?"
  • Variance Decomposition         • Z-score Anomaly Detection     • Natural Language Query
  • Rightsizing Rules              • Knapsack Budget Solver        • Pre-deployment Estimator
  • Hygiene Gamification           • Retrospective Simulator       • Grounded Chat Assistant
           │                               │                               │
           └───────────────────────────────┼───────────────────────────────┘
                                           ▼
                                [ SQLAlchemy ORM Layer ]
                            SQLite (local) / PostgreSQL (prod)
                                           │
           ┌───────────────────────────────┴───────────────────────────────┐
           ▼                                                               ▼
[ Synthetic Enterprise Engine ]                               [ Scoped AWS Integration ]
• NovaCart 180-day Time Series                                • IAM Cross-Account Role ARN
• 327 Multi-service Resources                                 • STS AssumeRole External ID
• CSV / JSON Ingestion Pipeline                               • Read-only Cost Explorer & CW
```

---

## 🏢 The NovaCart Enterprise Demo Scenario

To provide an internally consistent, CV-worthy demo experience, CloudWise AI comes pre-loaded with a realistic unicorn e-commerce infrastructure scenario (**NovaCart**):

| Metric | Value | Technical Context |
| :--- | :--- | :--- |
| **Monthly Spend** | **₹10,42,500** (~$12,500/mo) | 30-day run-rate across 8 AWS services |
| **Month-End Forecast** | **₹11,80,000** | Projected from 180-day trend & weekend seasonality |
| **Approved Budget** | **₹11,00,000** | **Expected overrun of +₹80,000** without intervention |
| **Identified Savings** | **₹1,63,000/month** | **₹19,56,000 annualized** across 8 high-confidence actions |
| **Active Anomalies** | **4 Incidents** | EC2 dev spike (+73%), NAT Gateway egress (+133%), etc. |
| **Tracked Resources** | **327 Resources** | Compute, DB, Storage, Cache, and Networking |
| **Engineering Teams** | **6 Teams** | Payments (#1, 88/100) down to AI/ML (#6, 64/100) |

---

## ⚡ Core Features & FinOps Flow

The application executes the 10-step conceptual loop:
$$\text{OBSERVE} \rightarrow \text{ANALYZE} \rightarrow \text{DETECT} \rightarrow \text{PREDICT} \rightarrow \text{EXPLAIN} \rightarrow \text{OPTIMIZE} \rightarrow \text{SIMULATE} \rightarrow \text{PRIORITIZE} \rightarrow \text{APPROVE} \rightarrow \text{VERIFY}$$

### 1. Flagship: "Why Did My Bill Increase?"
- Automated period-over-period variance decomposition.
- Breaks down exact dollar and percentage drivers (+₹1,59,500 / +18.1% MoM).
- Isolates forensic evidence: 18 unmanaged EC2 instances in `us-east-1`, 14TB cross-region S3 replication through NAT Gateway, and indefinite RDS snapshot drift.

### 2. Algorithmic Budget Optimization Solver
- Solves a **constrained multi-objective 0/1 Knapsack optimization problem**:
  $$\text{Minimize} \sum_{i \in S} \text{RiskWeight}_i \times \text{Effort}_i \quad \text{subject to} \quad \sum_{i \in S} \text{Savings}_i \ge \text{TargetSavings}$$
- Given a user target (e.g., *"I want to save ₹1,00,000/month with minimum risk"*), the solver evaluates all candidates and outputs the exact Pareto-optimal package.

### 3. ML Time-Series Cost Forecaster
- Combines linear growth regression, cyclical Fourier weekly seasonality, and residual variance modeling.
- Predicts 7-day, 30-day, and month-end spending with **80% and 95% confidence interval bands**.
- Quantifies budget overrun risk with a 91.4% model confidence score.

### 4. Statistical Cost Anomaly Detection
- Computes rolling 14-day median baselines and flags spend deviations ($Z > 2.5$ or $> 35\%$).
- Direct 1-click actions: Acknowledge, Investigate, Ask AI, or Convert into Optimization Recommendation.

### 5. Time-Travel Retrospective Simulator
- Counterfactual modeling answering: *"What if we had applied these recommendations 3 months ago?"*
- Compares actual invoices against simulated optimized curves, highlighting **₹1.1L in unrealized forgone savings**.

### 6. Forward-Looking What-If Simulator
- Elasticity modeling under traffic spikes (2x, 5x, 10x), server additions, and database resizing.
- Automatically flags infrastructure bottlenecks (e.g., *"Database IOPS saturation detected at RDS Primary under 3.5x scale"*).

### 7. Natural Language Pre-Deployment Cost Preview
- Shift-left cost awareness for developers.
- Interprets plain English prompts (e.g. *"I need a medium RDS PostgreSQL database in Mumbai"*) and returns instant monthly estimates, cost drivers, caveats, and cheaper alternatives.

### 8. Conversational AI Assistant & Voice Queries
- Grounded chatbot answering questions strictly from database records without hallucination.
- Supports **Web Speech API speech recognition** (voice-to-text) and optional **SpeechSynthesis audio readout**.

### 9. Cloud Hygiene Gamification
- Weighted FinOps score (0–100) per team and environment.
- Gamified leaderboard, badges (*"FinOps Champion"*, *"Zero Idle Waste"*, *"Tagging Master"*), and positive/negative factor attribution.

### 10. Human Approval & Savings Verification
- Multi-stage approval queue for all infrastructure changes.
- Automated Before vs. After verification table validating that post-change CPU and P99 latency remain stable while savings are realized.

---

## 🛠️ Tech Stack

- **Backend**: Python 3.13, FastAPI, SQLAlchemy 2.0, Pydantic V2, NumPy, Scikit-learn, Pandas, Uvicorn, Pytest.
- **Frontend**: React 19, TypeScript, Vite 6/8, Tailwind CSS v4, Recharts, Lucide Icons, Canvas Confetti.
- **Database**: SQLite default (zero-friction local execution) with native PostgreSQL support via standard `DATABASE_URL`.

---

## 🚦 Quickstart & Setup Guide

### 1. Prerequisites
- Python 3.11+
- Node.js v18+ and npm

### 2. Backend Setup
```bash
# Navigate to workspace
cd AI_CLOUD_COST

# Activate virtual environment
.\venv\Scripts\activate   # On Windows
# source venv/bin/activate # On Linux/macOS

# Install dependencies (already installed in venv)
pip install -r backend/requirements.txt

# Seed the NovaCart enterprise database
python backend/seed_data.py

# Start the FastAPI backend
python -m uvicorn app.main:app --app-dir backend --host 127.0.0.1 --port 8000 --reload
```
API Documentation will be live at: `http://127.0.0.1:8000/docs`

### 3. Frontend Setup
```bash
# In a second terminal:
cd AI_CLOUD_COST/frontend

# Install dependencies
npm install

# Start Vite development server
npm run dev
```
Web application will be accessible at: `http://localhost:5173`

---

## 🧪 Automated Testing

Run the automated backend test suite:
```bash
.\venv\Scripts\pytest -v
```
All tests verify cost calculations, forecasting bounds ($L_{80} \le \hat{y} \le U_{80}$), Knapsack solver optimality ($\ge ₹1,00,000$), anomaly detection, and API endpoints.

---

## 🔒 AWS Integration Architecture

CloudWise AI is architected for zero-trust enterprise deployment:
- Connects exclusively via AWS IAM Cross-Account Role with `sts:AssumeRole`.
- Requires an `ExternalId` token to prevent confused-deputy attacks.
- Scoped strictly to read-only permissions:
  - `ce:GetCostAndUsage`, `ce:GetCostForecast`
  - `cloudwatch:GetMetricData`, `cloudwatch:GetMetricStatistics`
  - `ec2:Describe*`, `rds:Describe*`, `s3:List*`
- **Zero Root Secrets**: No AWS access keys, secret keys, or passwords are ever stored or transmitted.

---

## 📜 Placement Walkthrough Checklist (5-Minute Demo Flow)

1. **Dashboard Overview**: Show spend (₹10.42L), month-end forecast (₹11.80L), and potential savings (₹1.63L/mo).
2. **AI Variance Breakdown**: Click *"Why Did My Bill Increase?"* to demonstrate period-over-period explanation (+18.1%) and root causes.
3. **Cost Explorer**: Filter by EC2 in Mumbai (`ap-south-1`) and drill down into the 327 resources.
4. **Optimization Recommendations**: Review rightsizing recommendation (`m5.2xlarge` $\rightarrow$ `m5.large`) with 89% confidence.
5. **Optimization Solver**: Input *"₹1,00,000/mo"* target and execute the knapsack solver to produce an optimal package.
6. **Cloud Hygiene Score**: Review the 6-team leaderboard (Payments Team #1 at 88/100).
7. **Time-Travel Simulation**: Slide 3 months back to demonstrate ₹1.1L in forgone savings.
8. **What-If Simulator**: Drag traffic to 5x to trigger the database IOPS bottleneck alert.
9. **Pre-Deployment Preview**: Type *"I need a medium RDS PostgreSQL in Mumbai"* and view instant estimates and cheaper Graviton alternatives.
10. **Voice Assistant**: Click the mic or submit *"Why is EC2 expensive?"* to show grounded citations.
11. **Approval & Savings Verification**: Authorize an optimization and inspect the Before vs. After verified savings record.
