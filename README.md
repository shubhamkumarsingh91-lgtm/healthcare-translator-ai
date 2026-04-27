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
outputs/multi_step_results.md
```

This helped evaluate:

* Structured reasoning ability
* Prompt-following accuracy
* Output consistency
* Model limitations

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

(Add here:)

* Open WebUI models
* Knowledge base setup
* Example outputs

---

## 💡 Motivation

Healthcare claim systems are complex and often difficult to understand.

This project explores how **AI can bridge the gap between technical systems and real users** by adapting responses based on context and role.

---

## ⚠️ Disclaimer

This is a learning and experimental project.
Not intended for real medical or billing decisions.

---

<img width="1437" height="459" alt="image" src="https://github.com/user-attachments/assets/cb3bd09d-dcd5-4d20-bc4c-3e3e9380072f" />
