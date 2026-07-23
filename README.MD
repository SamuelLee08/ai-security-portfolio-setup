# AI Security & Threat Modeling Portfolio
**Samuel Lee** | CIS / Cybersecurity @ James Madison University  
`CompTIA Network+` | `Security+ (In Progress)` | `Clearance Eligible`

---

## Executive Summary

> **Proof Statement:** > I test LLM applications the way an adversary would—probing for prompt injection, system prompt leakage, and sensitive data exposure using structured, text-based attack techniques mapped to the OWASP Top 10 for LLMs. As a backend AI engineering intern working hands-on with production LLM pipelines (Claude API, RAG systems), I understand these applications from the inside—where the trust boundaries sit and where they break.

---

## 🗺️ Portfolio Architecture & Sitemap

Below is the structural flow of this repository, mapping adversarial prompt testing directly to backend application defenses:

![Portfolio Sitemap Diagram](./docs/assets/sitemap-diagram.png)

---

## 🚀 Featured Case Study: LLM Trust Boundary Assessment

**Target System:** Claude 3.5 Sonnet Analyst Assistant  
**Vulnerability Focus:** `OWASP LLM07:2025` (System Prompt Leakage & Direct Prompt Injection)

### The Voice Card (Before & After)
* ❌ **Generic AI Draft:** *"I utilized advanced adversarial prompt engineering techniques to evaluate LLM vulnerabilities and implement robust remediation strategies for optimal data security."*
* ✅ **My Refined Version:** *"I broke the model using a fake system update string because LLMs read everything as one flat token stream. I fixed it by securing the trust boundary in code, not in the prompt."*

### Key Technical Findings
* **The Vulnerability:** Flat token stream interpretation allowed XML wrapper attacks and fake administrative commands (`<admin_override>`) to bypass prompt guardrails.
* **The Code-Level Defense:** Implemented application-layer input escaping, dynamic per-request cryptographic delimiters on the backend, and strict output filtering rather than relying on weak prompt-level rules.

👉 **[Read the Full Case Study & Backend Code →](./case-studies/llm-trust-boundary-assessment.md)**

---

## 📁 Portfolio Directory & Index

| Document / Asset | Focus Area | Description |
| :--- | :--- | :--- |
| 📄 **[LLM Trust Boundary Case Study](./case-studies/llm-trust-boundary-assessment.md)** | `OWASP LLM07:2025` | Deep-dive assessment, architecture breakdown, and backend Python remediation code. |
| 🪜 **[The Prompt Ladder](./prompt-engineering/prompt-ladder-owasp-llm07.md)** | Adversarial Prompting | 5-stage iterative progression from a weak baseline prompt to XML wrapper exploits. |
| 🛠️ **[System Architecture & Logs](./docs/claude-config.md)** | Target Pipeline & SOC Logs | Model parameters, Claude project configuration, and pressure-test chat logs. |
| ✍️ **[Personal Voice Guide](./docs/voice-guide.md)** | Style & Communication | Tone rules ("Direct, plain-spoken, sharp, no corporate fluff") and editing process. |

---

## 🛠️ Security & Engineering Stack

* **AI Security:** OWASP Top 10 for LLMs, Adversarial Prompt Analysis, Delimiter Escaping, Trust Boundary Verification.
* **Backend & LLM Engineering:** Python, Claude API (Anthropic SDK), RAG Pipelines, System Prompt Architecture.
* **Networking & Security Fundamentals:** CompTIA Network+, Security+ (In Progress), System Logging & SOC Alignment.
