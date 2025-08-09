📘 FSSAI KM Chatbot (Open Source, Google Colab Friendly)
A Generative AI Proof of Concept that lets you query FSSAI regulatory PDFs in plain English.
The chatbot retrieves relevant document sections and answers with source references.

Built entirely with open-source tools — runs locally or in Google Colab without paid APIs.

🚀 Features
📄 Upload multiple PDFs

🧠 Semantic search over document content

🤖 Uses TinyLLaMA (quantized, CPU-friendly) for local inference

📌 Every answer includes citations with page numbers

💻 Gradio UI for easy interaction

📌 Why a PDF Regulatory Chatbot?
Regulatory documents are long and complex, making it hard to quickly find specific standards or limits.
This chatbot removes that barrier:

💬 "What is the maximum pesticide residue allowed in packaged grains?"
⬇️
Returns the exact standard with source page reference.

🛠️ Tech Stack
UI: Gradio

Logic: LangChain
LLM: TinyLLaMA-1.1B-Chat (quantized)
Vector Store: FAISS (local, fast semantic search)
Embeddings: all-MiniLM-L6-v2 (SentenceTransformers)
Data Source: PDF upload

⚙️ Quick Start
Option 1: Run in Google Colab (Recommended)
Open in Colab:
Upload your FSSAI PDFs.
Ask your question in plain English.
Get answers + citations.

📂 How It Works
Upload PDFs → Extracts and cleans text from each page.
Chunking → Splits text into small overlapping sections for better retrieval.
Embeddings → Converts text chunks into vectors using all-MiniLM-L6-v2.
FAISS Search → Finds the most relevant document chunks.
LLM Response → TinyLLaMA generates a structured answer with bullet points + citations.

📝 Example Query
Q: "List all food additive limits mentioned in section 2.3"
A:
Additive X – Max limit: 200 ppm
Additive Y – Max limit: 50 ppm

📄 Sources:
doc.pdf (page 14)
doc.pdf (page 15)

⚠️ Notes
Works best with text-based PDFs (not scanned images).
TinyLLaMA runs on CPU — expect slower responses compared to GPU.
Use Colab for faster processing and easy file upload.
