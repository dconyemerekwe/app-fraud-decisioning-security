# Attack & Defence for First-Time Payee Decisioning in Real-Time Payments

This repository contains a full security analysis of a **first-time payee decisioning system** in real-time payments (RTP), focusing on how attackers could exploit weaknesses to enable **Authorised Push Payment (APP) fraud**, and how layered defences can reduce this risk.

This work is based on the COMP1806 Information Security coursework brief, expanded and polished into a standalone portfolio-ready research report.

---

## Scenario Summary

Banks use a decision service to risk-score a **first-time payee** and determine whether to allow, warn, hold or block a payment. If an attacker can push an unsafe version of the model, poison facts, or gain access to CI/CD, they can bypass these controls and automate APP fraud.

This project analyses:

- The decision service (rules + ML)
- CI/CD pipeline and promotion controls
- Risk facts and feature loaders
- Routing behaviour (allow / warn / hold / block)
- Attack paths and realistic adversary behaviour
- Technical and organisational control layers

---

## Contents of the Report

The PDF includes:

- **Asset Inventory**  
- **Weighted-Factor Asset Valuation (WFV)**  
- **Threat–Vulnerability–Asset (TVA) Grid**  
- **Quantitative Risk Calculations**  
- **CVSS-lite Vulnerability Scoring**  
- **MITRE ATTACK-style Attack Path**  
- **Attack Graph Design**  
- **Defences & Controls Map**  
- **Incident Response Plan**  
- **Quick APP-Fraud Policy**  
- **Executive Brief (residual risk & controls)**  
- **Reflective Learning Statement**

Each section contains tables, diagrams, calculations, and concise summaries aligned to industry-style security reporting.

---

## Key Findings

- The highest-risk scenario involves **unsafe promotion** of the decision service.
- Before controls, the scenario presents **High** inherent risk (≈ 80/100).
- With layered controls, residual risk reduces to **Medium** (≈ 40/100).
- Key security gaps include:
  - Phishable MFA
  - Weak CI/CD checks
  - Insufficient fact quality validation
  - Insufficient drift monitoring
- Recommended controls include:
  - FIDO/WebAuthn MFA
  - Two-person approvals + policy-as-code
  - Canary/shadow deployments with auto-rollback
  - Fail-closed routing behaviour
  - KPI guardrails and anomaly detection

---

## Skills Demonstrated

- Asset modelling and weighted valuation  
- Quantitative risk calculation (Likelihood × ASP × Loss × Asset Value)  
- CVSS-lite vulnerability scoring  
- MITRE ATTACK-based attack modelling  
- Attack graph design  
- CI/CD and identity security principles  
- Incident response playbook design  
- Security policy writing  
- Payment security & APP fraud domain knowledge  

---

## PDF Report

The full research document is included in:
[**Open the full research PDF**](./APP-Fraud-Decisioning-Attack-and-Defence.pdf)

---

## Module Context

- **Module:** COMP1806 – Information Security  
- **Institution:** University of Greenwich  
- **Year:** 2025  
- **Project Type:** Coursework
- **Author:** Destiny Onyemerekwe
