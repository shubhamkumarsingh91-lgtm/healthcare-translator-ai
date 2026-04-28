# 🧠 Healthcare Claims Assistant AI

### From Prompt-Based Translator → Agent-Style AI System

---

## 📌 Overview

This project started as a **Healthcare Claims Translator AI** and evolved into an **AI Claims Assistant Platform**.

It translates complex healthcare claim rejection messages into **structured, actionable outputs** tailored for different roles:

* 🏥 Providers (billing workflows)
* 🧑‍⚕️ Patients (simple explanations)
* 🧠 Analysts (technical debugging)

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

(Add here:)

* Open WebUI models
* Knowledge base
* Tool usage example

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
