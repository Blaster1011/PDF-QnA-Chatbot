# PDF QnA Chatbot

A chatbot that lets you upload any PDF and ask questions about its content.
Built using LLaMA-3, LangChain, and FAISS on Google Colab.

## How it works

1. A PDF is loaded and split into small chunks of text
2. Each chunk is converted into vector embeddings using HuggingFace
3. When you ask a question, the most relevant chunks are retrieved using FAISS similarity search
4. The retrieved chunks are passed to a fine-tuned LLaMA-3 model which generates an answer

## Tech Stack

- LLaMA-3 (unsloth/llama-3-8b-bnb-4bit) — fine-tuned using LoRA
- LangChain — document loading and text splitting
- FAISS — vector storage and similarity search
- HuggingFace Embeddings — text embeddings
- PyMuPDF — PDF loading
- Google Colab — runtime environment

## Features

- Fine-tunes LLaMA-3 using LoRA on the Alpaca dataset
- Loads and processes PDF documents
- Answers questions strictly based on the PDF content
- If the answer is not in the document, it says "I don't know"

## Requirements

Run on Google Colab with GPU enabled (T4 or higher recommended)
