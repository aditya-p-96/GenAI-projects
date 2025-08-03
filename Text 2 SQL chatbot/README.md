# 🧠 Text-to-SQL Chatbot (Open Source, Google Colab Friendly)

A **hands-on Generative AI POC** that lets you query **structured data (CSV)** in plain English — the chatbot converts your question into **SQL**, runs it, and shows the result.

Built entirely with **open-source tools** so you can run it locally or in **Google Colab** without paid APIs.

---

## 🚀 Features
- Upload **any CSV** file as your dataset
- Ask **natural language questions**
- Auto-generates **SQL queries**
- Executes SQL against the uploaded dataset
- Returns **results** (and optional charts)
- 100% **local** — no paid API required

---

## 📌 Why Text-to-SQL?
Most enterprise data is **structured** (tables, rows, columns).  
But for many business users, accessing it requires **writing SQL** or **waiting for analysts**.

Text-to-SQL bridges this gap:
> 💬 "What’s the total spend for January?"  
> ⬇️  
> `SELECT SUM(Spend) FROM data WHERE Month='Jan'`

---

## 🛠️ Tech Stack
- **UI:** [Gradio](https://gradio.app/) for interactive chatbot interface
- **Orchestration:** [LangChain](https://www.langchain.com/) for prompt handling
- **LLM:** [mrm8488/t5-base-finetuned-wikiSQL](https://huggingface.co/mrm8488/t5-base-finetuned-wikiSQL) (public, CPU-friendly)
- **Database:** SQLite (in-memory)
- **Data Source:** CSV upload

---

## 📂 Project Structure
├── t2s_chatbot.py # Google Colab notebook
├── schema.csv # Example schema for procurement dataset
├── data.csv # Example procurement dataset
└── README.md # This file

## ⚙️ Quick Start

### **Option 1: Run in Google Colab (Recommended)**
1. Open in Colab:  
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/text2sql-poc/blob/main/text2sql_chatbot.ipynb)
2. Upload your CSV file.
3. Ask your question in plain English.
4. See generated SQL + results.

🖼️ Example Queries
What’s the total spend for Jan?
Top 3 departments by spend
