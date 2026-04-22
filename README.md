**🚀 Healthcare Claims & EDI Translator AI**

🧠** Problem**

Healthcare systems rely on complex formats such as EDI 837, MMIS workflows, and policy-driven validation rules.

**This creates major challenges:**

Claim rejections are hard to understand

Providers struggle to fix billing errors

Analysts spend time decoding technical messages

Patients receive unclear explanations

> The core issue is translation of technical healthcare language into actionable understanding

**💡 Solution**

This project builds a persona-aware AI system that translates healthcare claim and EDI messages into clear, role-specific explanations.

**The system:**

Interprets claim rejection messages

Explains the issue in plain English

Suggests next steps

Adapts output based on user persona

Personas supported:

🧑‍⚕️ Patient

🏥 Provider (billing staff)

🧑‍💻 Analyst / Developer

⚙️ Tech Stack

**Models Used**

- Gemma 3 1B
- Qwen3 4B GGUF (Q4_K_M)

These models were selected to run locally on Apple Silicon with limited memory while still supporting role-based healthcare claim explanation tasks.

UI: Open WebUI

Document Parsing: Docling (PDF → Markdown)

Architecture: Retrieval-Augmented Generation (RAG)

Environment: Docker + macOS (M1)

Language: Python (for scripts & processing)

**🔒 Compliance & Ethics**

This project strictly follows responsible AI principles:

✅ Uses only public healthcare documentation (CMS, Medicaid, etc.)

✅ Uses synthetic examples for testing

❌ Does NOT use real patient data (PHI)

❌ Does NOT use internal Medicaid or employer data

👉 Designed to be safe, reproducible, and shareable

**📥 Sample Input**

Claim rejected: Member not eligible on date of service

**📤 Sample Outputs**

🧑‍⚕️ Patient

Your insurance coverage was not active on the date of your visit. Please contact your provider or insurance company to verify your eligibility.

**🏥 Provider**

Eligibility check failed. Verify the member ID and coverage dates before resubmitting the claim.

**🧑‍💻 Analyst**

Eligibility validation failed during claim processing. Check subscriber ID and coverage data in the eligibility system for alignment.

📂 Project Structure
kb_md/        # Processed markdown documents (from Docling)

tests/        # Synthetic claim scenarios

outputs/      # Evaluation results

scripts/      # Helper scripts

screenshots/  # Demo visuals

🧪 Evaluation Approach
Synthetic claim rejection scenarios

Multi-persona output comparison

Grounded responses only (no hallucinations)

Iterative improvement via RAG tuning

**🗺️ Roadmap**

Phase 1 (Current)

Basic Translator AI (RAG + personas)

Public document ingestion via Docling

Phase 2
Provider fix checklists

Structured troubleshooting guidance

Phase 3
MMIS workflow mapping

Claim lifecycle explanations

Phase 4
AI governance layer

Confidence scoring

Refusal handling for unsafe queries

**🎯 Goal**

To build an AI system that reduces operational friction in healthcare systems by making complex technical processes understandable and actionable.

**👨‍💻 Author**

Shubham Singh

**🧠 Why this project matters**

This is not just a chatbot.

It is an attempt to bridge the gap between:

Technical healthcare systems & Real-world usability

👉 Turning complexity into clarity using AI
## 📸 Demo

### Patient View

<img width="2878" height="1428" alt="image" src="https://github.com/user-attachments/assets/aba006c7-c169-4e96-b03e-9bddfc82ac21" />

### Provider View

<img width="2864" height="1402" alt="image" src="https://github.com/user-attachments/assets/48033b28-5694-4bc7-8586-ad0c3569ae74" />

### Analyst View

<img width="1432" height="701" alt="image" src="https://github.com/user-attachments/assets/a8b0a947-b4b6-4bb2-a6aa-d136a8e1255e" />

### Models in the OpenAI View

<img width="1431" height="690" alt="image" src="https://github.com/user-attachments/assets/5513b562-d110-4d7b-9ea4-cc96506e2b04" />

### Knowledge Base
<img width="1437" height="459" alt="image" src="https://github.com/user-attachments/assets/cb3bd09d-dcd5-4d20-bc4c-3e3e9380072f" />
