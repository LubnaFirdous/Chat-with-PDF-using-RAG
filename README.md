# Chat with PDF using RAG

## Overview
This project implements a **Retrieval-Augmented Generation (RAG) pipeline** to allow users to **chat with PDF documents**. It uses **FAISS for vector search**, **SentenceTransformers for embeddings**, and **Hugging Face models** for generating responses based on retrieved information.

## Features
- Extracts text from uploaded **PDF files** using `pdfplumber`
- Splits text into manageable **chunks** for embedding
- **Embeds and indexes** the chunks using `FAISS`
- Retrieves relevant document chunks using **semantic search**
- Uses **Hugging Face's FLAN-T5 model** for generating responses

## Prerequisites
Ensure you have the following installed:
- Python 3.8+
- `streamlit`
- `pdfplumber`
- `numpy`
- `faiss`
- `sentence-transformers`
- `langchain`
- `langchain-community`
- `HuggingFaceHub`

Install dependencies using:
```bash
pip install streamlit pdfplumber numpy faiss-cpu sentence-transformers langchain langchain-community huggingface_hub
```

## Usage
### 1. Run the Streamlit App
```bash
streamlit run app.py
```

### 2. Enter Your Hugging Face API Key
- Go to Hugging Face ([huggingface.co](https://huggingface.co/))
- Generate an API key from **Settings > Access Tokens**
- Enter it in the **Streamlit sidebar**

### 3. Upload PDF Files
- Click **Upload PDF files** and add your documents.

### 4. Ask Questions
- Type your question in the text box.
- Click **Get Answer** to retrieve relevant responses from the document.

## File Structure
```
📂 Chat_with_PDF_RAG
├── app.py  # Main Streamlit application
├── README.md  # Documentation
```

## Troubleshooting
- If the model fails to generate responses, ensure your **Hugging Face API key** is correct.
- If PDF text extraction fails, try a **different PDF parser**.
- If results are inaccurate, **increase chunk size** in `RecursiveCharacterTextSplitter`.

## Future Improvements
- Implement **multi-document retrieval**
- Add **support for more LLMs**
- Improve **query relevance ranking**

## License
This project is open-source under the **MIT License**.

