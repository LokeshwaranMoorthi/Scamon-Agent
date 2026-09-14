#  Scamon-Agent — Autonomous Multi-Agent SOC for Cross-Vector Cyber Fraud Investigation

> **Cross-Vector Cyber Fraud Investigation, Real-Time Threat Correlation, and SHA-256 Cryptographic Evidence Vaulting.**

---

##  The Core Problem

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

##  The Scamon-Agent Solution

**Scamon Agent** replaces fragmented single-point tools with a **Collaborative Multi-Agent Forensics Network**. Instead of relying on a monolithic LLM, Scamon-Agent orchestrates independent micro-agents. Each agent operates as an autonomous investigator inspecting its dedicated threat vector before streaming telemetry to a centralized **Threat Correlation Engine** and a **SHA-256 Cryptographic Evidence Vault**.

---

## Key Features

- **True Multi-Agent Architecture** — Specialized agents instead of one bloated prompt
- **Real-time Live Call Analysis** via WebSockets + Whisper STT
- **Explainable Risk Scoring** — Every decision is transparent
- **Tamper-proof Evidence Chain** — SHA-256 hashing at ingestion
- **One-click Legal Output** — Ready-to-submit cybercrime complaints
- **Enterprise SOC Dark UI** — Built for high-speed investigation

---
# Micro-Agent Breakdown

| Agent Module          | Responsibilities & Protocol Audit                                                                 | Key Tech Stack                  |
|-----------------------|---------------------------------------------------------------------------------------------------|---------------------------------|
| Website Agent         | Audits WHOIS age, SSL handshakes, domain typosquatting distance, and blacklist registries.       | whois, ssl, Levenshtein Distance |
| Email Agent           | Parses raw SMTP headers, validates SPF/DKIM/DMARC alignment, and tracks relay hops.              | dnspython, Header Regex, Groq   |
| SMS Agent             | Captures active web message streams and evaluates incoming smishing text payloads.               | Selenium, FastAPI, Llama 3.1    |
| Visual Agent          | Performs OCR on image overlays, decodes QR targets, and detects brand logo spoofs.               | pytesseract, OpenCV, Pillow     |
| Call Agent            | Runs chunked WebSockets real-time audio analysis to detect urgency and vishing pressure.         | WebSockets, Whisper STT, Groq   |
| Correlation Engine    | Synthesizes telemetry across all agents to calculate centralized risk classifications.           | Weighted Scoring Pipeline       |
| Evidence Vault        | Hashes every ingested artifact with SHA-256 to guarantee immutable legal integrity.              | hashlib, MongoDB                |
| Complaint Agent       | Generates court-ready cybercrime complaint packages in PDF and DOCX formats.                     | reportlab, python-docx          |

---

# Single LLM vs. Scamon-Agent Architecture

| Feature / Metric       | Monolithic Single LLM                          | Scamon-Agent Multi-Agent                          |
|------------------------|------------------------------------------------|---------------------------------------------------|
| Architecture           | Single giant prompt handling all inputs        | Orchestrated specialized sub-agents               |
| Parsing Precision      | Low (mixes DNS, Headers, Audio)                | High (isolated protocol parsers)                  |
| Execution Model        | Sequential only                                | Fully Asynchronous / Parallel                     |
| Fault Isolation        | Single payload error crashes run               | Partial vector scans still succeed                |
| Context Bloat          | High token bloat & context drift               | Minimal, vector-specific context windows          |

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

---
