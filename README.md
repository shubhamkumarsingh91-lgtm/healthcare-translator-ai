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
LLM: Ollama (local models like Gemma / Qwen)
UI: Open WebUI
Document Parsing: Docling (PDF → Markdown)
Architecture: Retrieval-Augmented Generation (RAG)
Environment: Docker + macOS (M1)
Language: Python (for scripts & processing)
🔒 Compliance & Ethics

This project strictly follows responsible AI principles:

✅ Uses only public healthcare documentation (CMS, Medicaid, etc.)
✅ Uses synthetic examples for testing
❌ Does NOT use real patient data (PHI)
❌ Does NOT use internal Medicaid or employer data

👉 Designed to be safe, reproducible, and shareable
