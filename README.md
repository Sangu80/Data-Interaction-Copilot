# Data-Interaction-Copilot

# 🤖 Data-Interaction Copilot – A Smarter Way to Explore Data

![copilot-banner](assets/banner.gif) <!-- Replace with actual image path -->

Welcome to my submission for **Part 2B** of the **Data Science Coding Test – 12 May 2025**. This project is a compact, schema-aware data assistant — think of it as an "EDA Copilot" powered by large language models (LLMs), built for analysts who want powerful, conversational control over their data.

---

## 🚀 What It Does

This copilot allows users to explore tabular datasets using natural language. It provides an interactive command-line interface where prompts like:

> `"What are the top 5 features with missing values?"`

or

> `"Simulate a 0.5% increase in interest rates and show the impact on loan status"`  

...are translated into real, pre-validated actions like SQL queries, pandas transformations, or simulations.

---

## 🛠 Features

| Capability                  | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| ✅ **Schema Awareness**     | Understands and uses dataset schema for intelligent prompts and validation |
| 💬 **Natural Language UI**  | Uses OpenAI’s API to interpret and map user queries to executable commands |
| 🧪 **Secure Sandbox**       | All LLM calls are guarded — no dynamic `exec()` or `eval()`                |
| 🔄 **Interactive Shell**    | Run `python your_tool.py` to start an interactive session                  |
| 🧩 **Fallback Support**     | Works even without an OpenAI key (manual commands)                         |
| 📊 **EDA Utilities**        | Built-in functions for quick insights, summaries, and simulations          |
| ✨ **Portable**             | Cross-platform compatible, ≤ 400 logical lines                             |

---

## 📂 Project Structure

data-copilot/
│
├── your_tool.py # Main tool – single self-contained file
├── requirements.txt # Exact dependencies
├── .env.example # Template for API keys
├── demo.gif # [Optional] 2-min demo screencast
├── assets/
│ ├── banner.gif # Copilot banner / visual
│ └── screenshots.png # Additional UI or CLI visuals
└── README.md


---

## 🎬 Demo

![demo](assets/demo.gif) <!-- Replace with your actual demo image or screencast -->

> _"See it in action!"_  
Live demo screencast showing two interactions — schema understanding and a portfolio simulation.

---

## 🧠 Design Decisions

- Built a lightweight **command registry** to ensure **LLM safety** and controlled execution
- Provided **fallback CLI commands** to allow full functionality without an API key
- Focused on **modular actions** (EDA summary, column stats, simulations) to encourage reusability
- Kept it under **400 lines**, with clean docstrings and in-code comments

---

## 💡 Possible Extensions

- Add **Pinecone / Weaviate** for vector search over schemas
- Embed **streamlit** or **Gradio UI** front-end for a visual interface
- Expand to support **multi-table joins** and basic **forecasting capabilities**

---

## 📦 Setup & Usage

### Step 1: Clone and Install

```bash
git clone https://github.com/yourusername/data-copilot.git
cd data-copilot
pip install -r requirements.txt

### Step 2: Add Your API Key
bash
Copy
Edit
cp .env.example .env
# Open .env and add your OpenAI API key

Step 3: Launch the Copilot
bash
Copy
Edit
python your_tool.py

🔒 Safety First
No eval(), exec(), or shell command execution.
Only whitelisted functions are allowed to run via the LLM interface.

---

✅ **To finish setup**:
- Replace image paths like `assets/banner.gif`, `assets/demo.gif`, or `assets/screenshots.png` with your actual files.
- Change the GitHub repo URL (`https://github.com/yourusername/...`) to your own.
- You can also embed the GIF using raw GitHub CDN links or use an external host like Imgur if preferred.

Let me know if you'd like a `requirements.txt`, `.env.example`, or help writing unit tests next!
