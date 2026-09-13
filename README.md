# 🛡️ Scamon Agent — Enterprise Multi-Agent Deception & Forensics Network

> **Cross-Vector Cyber Fraud Investigation, Real-Time Threat Correlation, and SHA-256 Cryptographic Evidence Vaulting.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-green.svg)](https://fastapi.tiangolo.tech/)
[![React](https://img.shields.io/badge/React-18.0+-61DAFB.svg)](https://react.dev/)
[![Architecture](https://img.shields.io/badge/Architecture-Multi--Agent--Orchestration-orange.svg)]()

---

## 🚨 The Core Problem

Modern cyber-fraud is no longer confined to static phishing links. Scammers deploy highly sophisticated, **multi-channel social engineering campaigns** combining:
* Spoofed SMS messages (Smishing)
* Malicious domain registrations with self-signed SSL certs (Typosquatting)
* Cloned voice calls with verbal pressure tactics (Vishing)
* Visual brand impersonations and malicious QR code payment hooks

**Why traditional defenses fail:**
1. **Channel Isolation:** Legacy security products analyze threat channels in silos, missing cross-vector linkages.
2. **Monolithic LLM Fragility:** Single giant prompts suffer from severe context bloat, high latency, and protocol-parsing hallucinations when handling mixed media.
3. **Chain-of-Custody Loss:** Unverified logs and unstructured AI summaries are inadmissible for formal legal complaints or police filings.

---

##  The Scamon Agent Solution

**Scamon Agent** replaces fragmented single-point tools with a **Collaborative Multi-Agent Forensics Network**. Instead of relying on a monolithic LLM, ScamON orchestrates independent micro-agents. Each agent operates as an autonomous investigator inspecting its dedicated threat vector before streaming telemetry to a centralized **Threat Correlation Engine** and a **SHA-256 Cryptographic Evidence Vault**.

---

##  System Architecture

```text
                               ┌───────────────────────────┐
                               │     Master Orchestrator   │
                               └─────────────┬─────────────┘
                                             │
      ┌───────────────────┬──────────────────┼───────────────────┬───────────────────┐
      ▼                   ▼                  ▼                   ▼                   ▼
┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌─────────────────┐
│ Website Agent│   │  Email Agent │   │  SMS Agent   │   │ Visual Agent │   │ Live Call Agent │
│ (WHOIS/SSL)  │   │(DKIM/Headers)│   │ (Stream Sync)│   │  (OCR/QR)    │   │ (WebSockets WS) │
└──────┬───────┘   └──────┬───────┘   └──────┬───────┘   └──────┬───────┘   └────────┬────────┘
       │                  │                  │                   │                   │
       └──────────────────┴──────────────────┼───────────────────┴───────────────────┘
                                             ▼
                               ┌───────────────────────────┐
                               │ Threat Correlation Engine │
                               └─────────────┬─────────────┘
                                             │
                       ┌─────────────────────┴─────────────────────┐
                       ▼                                           ▼
         ┌───────────────────────────┐               ┌───────────────────────────┐
         │ Cryptographic Vault       │               │ Complaint & XAI Engine    │
         │ (SHA-256 Hashed Evidence) │               │ (Auto-PDF & Multilingual) │
         └───────────────────────────┘               └───────────────────────────┘
