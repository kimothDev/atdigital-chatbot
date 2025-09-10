# AT Digital Chatbot

A simple **CLI chatbot** that answers questions using content from AT Digital’s website.

---

## Overview
This chatbot allows users to ask questions about AT Digital’s services, team, blog, and contact info. It returns the most relevant page content along with the source.

- **Dataset:** AT Digital website JSON.  
- **Embeddings:** Generated locally using Hugging Face’s `sentence-transformers` model [`all-MiniLM-L6-v2`](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2).  
- **Interface:** CLI loop in a Colab notebook.

---

## Getting Started
1. Clone the repository or open the notebook directly in Colab:
 ```bash
   git clone https://github.com/kimothDev/atdigital-chatbot.git
  ```
2. Open the notebook: `AT_Digital_Chatbot.ipynb`.  
3. Run all cells **from top to bottom**.  
4. When prompted, type your questions in the input field.  
5. To exit the chatbot, type:
 ```bash
   exit
  ```
---

## Dependencies 
- `sentence-transformers`  
- `numpy`  

---

## How it Works

1. Load JSON dataset; combine each page name with its text.
2. Generate sentence embeddings for all entries using Hugging Face all-MiniLM-L6-v2
3. Embed user query and compute cosine similarity with dataset embeddings.
4. Return the most relevant answer with page name and URL.
