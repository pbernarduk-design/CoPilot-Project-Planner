# Project Management Plan Generator (Streamlit)

A lightweight web app that generates a structured **Project Management Plan** starting from your desired **outcome**. It guides you through **Objectives**, **Governance**, and **Risks**, then compiles everything into a clean document you can export as **DOCX** or **Markdown**.

## ✨ Features
- Outcome-first prompts
- Objectives (SMART-style guidance)
- Governance (roles, cadence, escalation, optional RACI)
- Risks (industry/method-aware suggestions, P×I scoring)
- Milestones, Stakeholders & Communications, Success Measures
- Export to **DOCX** and **Markdown**

## 🚀 Quick start

### Run locally
```bash
pip install -r requirements.txt
streamlit run app.py
```

### Deploy to Streamlit Community Cloud
1. Push this folder to a **GitHub** repository (public or private).
2. Go to https://streamlit.io/cloud → **New app** → pick your repo.
3. Set **Main file path** to `app.py` and deploy.

> **Defaults**: Methodology = **Hybrid**, Industry = **Information Technology / Software**.

## 🛠️ Customize
- Add/modify industry risks in `BASE_RISKS` inside `app.py`.
- Adjust governance roles by editing `DEFAULT_GOV_ROLES`.
- Change theme in `.streamlit/config.toml`.
- (Optional) Add LLM-based narrative expansion later via `.streamlit/secrets.toml`.

## 📁 Project structure
```
pm-plan-generator/
├─ app.py
├─ requirements.txt
├─ README.md
├─ .gitignore
└─ .streamlit/
   ├─ config.toml
   └─ secrets.toml.example
```

## 🔐 Secrets (optional, for future enhancements)
Create `.streamlit/secrets.toml` (NOT committed) from the provided example if you add integrations:
```toml
# .streamlit/secrets.toml
AZURE_OPENAI_API_KEY = "..."
AZURE_OPENAI_ENDPOINT = "https://..."
```

## 🧪 Health check
If deployment fails on Streamlit Cloud, check the app logs and ensure the Python version is compatible with the pinned packages.

## 📜 License
MIT License – see `LICENSE`.
