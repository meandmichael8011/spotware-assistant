# Agentic RAG System — Spotware Assessment Submission

Dear Spotware Assessor,  
Thank you in advance for your time and effort in reviewing this project.

---

## 🧠 Project Overview

This repository contains all the code for an **AI-driven agentic RAG system**.

To showcase **multi-step reasoning and agentic flow**, the agent operates over public financial information using:

- Common currency knowledge
- Yahoo Finance API
- Dynamic visualizations

The system is powered by **three tools**:

1. **General Currency Info Tool**  
   Uses similarity search over embedded documents (powered by `Voyage-3-large`, chosen for its superior retrieval performance).

2. **Currency Price Lookup Tool**  
   Fetches open/close values for currency pairs (including crypto) via the **Yahoo Finance API**.

3. **Currency Chart Visualization Tool**  
   Dynamically generates and stores visual outputs as `.png` images.

---

## ⚙️ Setup Instructions

This project requires **Python 3.12**. All dependencies are listed in `requirements.txt`, and you'll need to provide **two API keys** via a `.env` file:

- `OPENAI_API_KEY`
- `VOYAGE_API_KEY`

> 💡 The token usage is minimal.

### 🔧 Local Setup (Recommended)

To run locally in a virtual environment:

```bash
# 0. Unzip the archive in a directory of your choice
# 1. Create and activate virtual environment
python -m venv env
source env/bin/activate  # On Windows, use `env\Scripts\activate`

# 2. Navigate into the project folder
cd your_project_directory

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the Streamlit app
streamlit run aprod.py
