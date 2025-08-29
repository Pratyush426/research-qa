# 📄 Research QA Bot – Chat with Your Papers

A **Streamlit-powered AI Assistant** that lets you upload **Multiple** research papers (PDFs) and **ask natural language questions** about them.  
No more manual skimming through dozens of pages — this bot extracts, chunks, embeds, and retrieves the most relevant context from your PDFs and generates concise, accurate answers.

---

## 🚀 Features

* 📂 Upload multiple research papers in PDF format  
* 🔍 Extracts and preprocesses text from PDFs  
* ✂️ Splits content into **semantic chunks** for better retrieval  
* 📊 Uses **FAISS Vector Store** for efficient similarity search  
* 🧠 Powered by **Google Generative AI (Gemini & Embeddings)**  
* 💬 Interactive **Q&A chat interface** with Streamlit  
* ⚡ Accurate, context-aware answers with guardrails against hallucinations  

---

## 🛠️ Tech Stack

* **Python 3.10+**  
* [Streamlit](https://streamlit.io/) – UI for user interaction  
* [PyPDF2](https://pypi.org/project/PyPDF2/) – PDF text extraction  
* [LangChain](https://www.langchain.com/) – Text chunking & QA chain  
* [FAISS](https://github.com/facebookresearch/faiss) – Vector store for semantic search  
* [Google Generative AI](https://ai.google.dev/) – Embeddings & Gemini LLM  
* [dotenv](https://pypi.org/project/python-dotenv/) – Manage API keys securely  

---

## 📂 Project Pipeline

Here’s the step-by-step **data flow pipeline** that powers the bot:  

1. **PDF Upload** – User uploads one or more research papers via Streamlit.  
2. **Text Extraction** – Extract raw text from each page using **PyPDF2**.  
3. **Text Chunking** – Break text into overlapping chunks using **RecursiveCharacterTextSplitter** (helps preserve context).  
4. **Embeddings Generation** – Convert text chunks into embeddings using **Google Generative AI Embeddings**.  
5. **Vector Store Indexing** – Store embeddings in a **FAISS index** for efficient similarity search.  
6. **User Query** – User asks a question in natural language.  
7. **Retrieval** – Relevant chunks are fetched from FAISS.  
8. **Answer Generation** – Context + query passed to **Gemini LLM** via LangChain for structured, accurate answers.  
9. **Streamlit UI** – Display answers in real-time.  

---

## ⚡ Quickstart

### 1️⃣ Clone the Repo
```bash
git clone https://github.com/your-username/research-qa-bot.git
cd research-qa-bot
````

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Set up Environment Variables

Create a `.env` file in the root directory and add your **Google API key**:

```bash
GOOGLE_API_KEY=your_api_key_here
```

### 4️⃣ Run the App

```bash
streamlit run app.py
```

### 5️⃣ Upload PDFs & Ask Questions!

* Upload one or multiple research papers.
* Type your question in the input box.
* Get concise, context-aware answers instantly.


