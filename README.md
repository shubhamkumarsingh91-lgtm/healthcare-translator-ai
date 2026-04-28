# 🧠 Healthcare Claims Assistant AI (Local RAG System)

## 📌 Overview

This project is a **local AI-powered healthcare claims assistant** designed to translate and analyze claim rejection messages for different users:

* 🧑‍⚕️ Patients → simple explanations
* 🏥 Providers → operational billing guidance
* 🧠 Analysts → technical debugging insights

The system uses **persona-based prompting + structured knowledge base (RAG)** to generate grounded and actionable responses.

---

## 🧩 Key Features

* ✅ Persona-based AI (Patient / Provider / Analyst)
* ✅ Structured healthcare knowledge base (Markdown)
* ✅ Retrieval-Augmented Generation (RAG)
* ✅ Multi-step prompt testing
* ✅ Automated testing pipeline (Python script)
* ✅ Local LLM execution (no external APIs)

---
## 🚀 Upgrades Key Features

- Multi-agent AI (Provider, Analyst, Patient)
- RAG-based knowledge system
- Tool-integrated reasoning (eligibility check)
- Structured output enforcement
- Advanced testing pipeline

## 🏗️ System Architecture

```text
**User Input
   ↓
System Prompt (Persona)
   ↓
Knowledge Base (RAG)
   ↓
Local LLM (Ollama)
   ↓
Structured Output**
```

---

## 🏗️ New Upgraded System Architecture

The project has evolved from a simple healthcare claims translator into an early-stage **AI Claims Assistant Platform**.

### Architecture Flow

```text
User Claim Rejection Input
        ↓
Open WebUI Model Interface
        ↓
Persona System Prompt
(Patient / Provider / Analyst)
        ↓
Knowledge Base Retrieval (RAG)
        ↓
Tool Layer
(e.g., eligibility check)
        ↓
Local LLM via Ollama
(Qwen / Gemma)
        ↓
Structured Role-Based Output


## 👥 Persona-Based Design

Each role uses a dedicated system prompt:

### Patient Translator

* Explains rejections in simple terms
* Focuses on clarity and next steps

### Provider Translator

* Provides operational checklist
* Focuses on billing workflows and verification

### Analyst Translator

* Provides technical interpretation
* Focuses on debugging and system validation

---

## 📚 Knowledge Base (RAG)

The system uses structured markdown files:

```text
Claims_Translator_KB
- eligibility.md
- coding.md
- provider.md
- authorization.md
- rejection_mapping.md
- cause_fix_mapping.md
```

### Benefits:

* Improved accuracy
* Reduced hallucination
* Consistent outputs

---

## 🧪 Testing Approach

### Multi-Step Prompt Testing

I created structured prompts to test model reasoning:

```text
Example:
Claim rejected: Missing prior authorization

1. Explain for provider
2. Identify root cause
3. List what to verify
4. Suggest next action
```

---

### Automated Testing Script

```bash
scripts/run_tests.py
```

* Runs multiple prompts
* Tests all personas
* Saves outputs automatically

---

### Results

```bash
## 🧪 Advanced Testing

This project includes advanced test scenarios to evaluate real-world AI behavior.

### Test Files

- `tests/advanced_test_scenarios.md`  
  Contains multi-step and edge-case claim rejection scenarios.

- `outputs/advanced_test_results.md`  
  Stores model outputs and evaluation notes.

---

### What is being tested

These scenarios evaluate:

- Multi-step reasoning  
- Tool usage (eligibility check)  
- RAG grounding (knowledge base usage)  
- Conflict handling (tool vs claim rejection)  
- Structured provider workflows  

---

### Example Scenario

**Input:**

Claim rejected: Member not eligible. Check eligibility for member ID 12345. Use the tool result as source of truth. Explain the likely cause, what to verify, next action, and missing information.

Output:

The rejection message "Member not eligible" may be a misclassification, as the eligibility tool result for member ID 12345 is **ACTIVE** [1]. This indicates the member is eligible, so the rejection likely stems from a mismatch between the submitted claim data and the payer’s current eligibility record.  

**What to verify**  
- Confirm the **date of service** on the claim aligns with the member’s coverage period.  
- Verify the **member ID** matches the one on the insurance card and payer records.  
- Check if the **payer and plan details** selected during submission match the current eligibility record.  

**Next action**  
Resubmit the claim after correcting any discrepancies in the claim data (e.g., date of service, member ID, payer plan) and confirming eligibility for the exact date of service.  

**Missing information**  
The specific **date of service** and **payer response details** are needed to fully diagnose the mismatch.

**Expected Behavior:**
- Use tool output as source of truth  
- Avoid hallucination (no fake error codes)  
- Provide structured operational steps  

---

### Why this matters

These tests ensure the AI system behaves like a real-world healthcare analyst:
- Accurate  
- Consistent  
- Actionable  
- Reliable under complex conditions

---

## ⚙️ Tech Stack

* Open WebUI (local AI interface)
* Ollama (LLM runtime)
* Python (requests, testing scripts)
* Markdown (knowledge base)
* GitHub (version control)

---

## 🤖 Models Used

| Model                  | Size         | Usage               |
| ---------------------- | ------------ | ------------------- |
| Qwen3 4B (GGUF Q4_K_M) | ~4B params   | Primary model       |
| Gemma 1B–3B            | Small models | Lightweight testing |

### Notes:

* Runs locally on MacBook (CPU-based)
* Performance varies with model size
* Larger models improve reasoning but increase latency

---

## 📊 Example Output (Provider)

```text
Claim rejected: Missing prior authorization

1. Likely cause:
Procedure requiring prior authorization was billed without approval.

2. What to verify:
- Check payer portal for authorization requirement
- Verify submission before service date
- Confirm provider NPI matches authorization

3. Next action:
- Submit retro-authorization if allowed
- Attach clinical documentation
- Resubmit claim
```

---

## 🧠 Key Learnings

* Prompt structure strongly impacts output quality
* Multi-step prompts reveal model limitations
* Smaller models require more explicit instructions
* RAG improves grounding but requires clean data
* Persona-based design improves usability

---

## 🔧 Current Focus (Based on Feedback)

Following AI engineer recommendations:

* ✔ Multi-step prompt testing (completed)
* ✔ Model transparency added (this README)
* 🔄 Improving operational accuracy of outputs
* 🔄 Exploring Skills (prompt modularization)

---

## 🚀 Next Steps

* Improve output precision (reduce redundancy)
* Add more complex multi-step scenarios
* Expand Skills (task-based prompting)
* Explore Tools (function-based automation)
* Add lightweight UI/dashboard

---

## 📸 Screenshots

* Open WebUI models
* <img width="1439" height="801" alt="image" src="https://github.com/user-attachments/assets/8873cc26-e731-4bf2-8399-bf9053a7d793" />

* <img width="1407" height="800" alt="image" src="https://github.com/user-attachments/assets/168eb4dd-b7d4-49be-8d1d-6236043983b7" />

* Knowledge base setup
* <img width="1428" height="805" alt="image" src="https://github.com/user-attachments/assets/4dd63ef3-da49-4a7f-903f-bf4fc446766c" />

* Example outputs
# Provider AI Assistant
  <img width="1432" height="713" alt="image" src="https://github.com/user-attachments/assets/f6350351-7594-43c7-becb-b5f728bb83c8" />


---

## 💡 Motivation

Healthcare claim systems are complex and often difficult to understand.

This project explores how **AI can bridge the gap between technical systems and real users** by adapting responses based on context and role.

---

## ⚠️ Disclaimer

This is a learning and experimental project.
Not intended for real medical or billing decisions.

--
