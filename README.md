# 🧠 Healthcare Claims Assistant AI

### From Prompt-Based Translator → Agent-Style AI System

---

## 📌 Overview

## ❗ Problem

Healthcare claim rejections are complex, technical, and difficult to interpret.

* Providers struggle to understand rejection reasons and next steps
* Patients receive unclear explanations
* Analysts spend time debugging issues manually
* Existing systems provide raw error codes without actionable guidance

This leads to:

* delayed claim processing
* increased operational cost
* poor communication between stakeholders

---

## 💡 Solution

This project builds an **AI Claims Assistant** that:

* translates claim rejection messages into structured, actionable insights
* adapts explanations based on user role (Provider, Patient, Analyst)
* uses a knowledge base (RAG) for grounded responses
* integrates tools (e.g., eligibility check) for validation
* enforces structured outputs for operational clarity

The goal is to move from **raw error messages → intelligent, guided workflows**

## 📌 Overview

This project is an **AI-powered Healthcare Claims Assistant** designed to help users understand and resolve claim rejection issues.

It transforms complex claim rejection messages into **clear, structured, and actionable outputs** tailored for different roles:

* 🏥 Providers → operational billing guidance
* 🧑‍⚕️ Patients → simple explanations
* 🧠 Analysts → technical debugging insights

The system combines:

* persona-based prompting
* retrieval-augmented generation (RAG)
* tool-based validation

to simulate real-world healthcare claim workflows.

## 🎯 Project Goal

The goal of this project is to move beyond simple AI responses and build a system that:

* understands claim rejection context
* reasons through multiple conditions
* validates information using tools
* produces structured, actionable workflows

This is an early step toward building a **real AI assistant for healthcare operations**, not just a chatbot.
---

# 🚀 Project Evolution

## 🔹 Version 1 — Basic Translator (Initial Build)

### What it did:

* Converted claim rejection messages into human-readable explanations
* Used simple prompts with local LLMs
* Generated outputs for different personas

### Limitations:

* No structured testing
* No knowledge grounding
* High chance of hallucination
* Generic outputs

---

## 🔹 Version 2 — Structured AI System (Current)

### Major Improvements:

### ✅ 1. Persona-Based Architecture

* Separate system prompts for:

  * Provider
  * Patient
  * Analyst
* Role-specific outputs

---

### ✅ 2. Knowledge Base (RAG)

* Structured markdown files:

```text
kb_md/
- eligibility.md
- coding.md
- provider.md
- authorization.md
- rejection_mapping.md
- cause_fix_mapping.md
```

👉 Improves:

* accuracy
* consistency
* explainability

---

### ✅ 3. Multi-Step Prompt Testing

* Designed prompts with multiple instructions:

```text
Explain → Identify cause → Verify → Next action
```

* Helps evaluate:

  * reasoning ability
  * prompt-following
  * output structure

---

### ✅ 4. Automated Testing Pipeline

```bash
scripts/run_tests.py
```

* Runs multiple scenarios
* Tests all personas
* Saves outputs to:

```bash
outputs/multi_step_results.md
```

---

### ✅ 5. Advanced Test Scenarios

```bash
tests/advanced_test_scenarios.md
outputs/advanced_test_results.md
```

Covers:

* multi-issue claims
* conflicting data scenarios
* edge cases
* real-world workflows

---

### ✅ 6. Tool Integration (Agent Behavior)

Implemented a custom tool:

```python
check_eligibility(member_id)
```

👉 Enables:

* system to validate eligibility
* reduces hallucination
* introduces decision-based reasoning

---

### ✅ 7. Controlled Reasoning

Improved system prompts to:

* prioritize tool output as source of truth
* prevent hallucinated error codes
* enforce structured outputs

---

# 🏗️ System Architecture

```text
User Input
   ↓
Open WebUI (Model Interface)
   ↓
Persona System Prompt
   ↓
Knowledge Base (RAG)
   ↓
Tool Layer (Eligibility Check)
   ↓
Local LLM (Ollama - Qwen / Gemma)
   ↓
Structured Output
```

---

# ⚙️ Tech Stack

* Open WebUI
* Ollama (local LLM runtime)
* Qwen3 4B (GGUF)
* Gemma (lightweight testing)
* Python (requests, scripts)
* Markdown (knowledge base)
* GitHub

---

# 🧪 Example Output (Provider)

```text
Claim rejected: Member not eligible

1. Likely cause:
Mismatch between claim data and payer eligibility system.

2. What to verify:
- Member ID accuracy
- Date of service coverage
- Payer system record

3. Next action:
Verify eligibility in payer portal and resubmit corrected claim.
```

---

# 🧠 Key Learnings

* Prompt structure significantly impacts output quality
* Multi-step prompts expose model limitations
* Tool integration improves reliability
* RAG reduces hallucination but requires structured data
* Persona-based design improves usability

---

# 🚀 Current Focus

Based on feedback:

* ✔ Multi-step testing
* ✔ Model transparency
* ✔ Tool integration
* 🔄 Improving operational accuracy
* 🔄 Expanding advanced scenarios

---

# 🔮 Next Steps

* Add more tools (authorization, coding validation)
* Improve workflow chaining (multi-step reasoning)
* Explore Skills (modular prompts)
* Build UI/dashboard layer
* Move toward production-ready system

---

# 📸 Screenshots

* Open WebUI models
<img width="1433" height="857" alt="image" src="https://github.com/user-attachments/assets/d8cb260c-7593-42c8-ab13-1dd585491e07" />

* Knowledge base
<img width="1438" height="799" alt="image" src="https://github.com/user-attachments/assets/1307d898-88af-473c-b6ec-73ba6af58aef" />

<img width="1430" height="812" alt="image" src="https://github.com/user-attachments/assets/430420ce-c786-485a-b5ef-7c45dfb6e682" />

<img width="1440" height="793" alt="image" src="https://github.com/user-attachments/assets/22e3f442-4cbb-4bf5-8305-f255d533d310" />


* Tool usage example

<img width="1440" height="808" alt="image" src="https://github.com/user-attachments/assets/1bacd2c5-d419-46d0-b84e-bfc9a3524581" />

<img width="1435" height="855" alt="image" src="https://github.com/user-attachments/assets/70fa27fd-f9f1-4f65-a288-8f9ffc0a7813" />


---

# 💡 Goal

To build a **practical AI system for healthcare claims processing** that combines:

* reasoning
* structured knowledge
* tool-based validation

---

# ⚠️ Disclaimer

This is an experimental learning project.
Not intended for real medical or billing decisions.

---

# 🔗 GitHub

https://github.com/shubhamkumarsingh91-lgtm/healthcare-translator-ai
