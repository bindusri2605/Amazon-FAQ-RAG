# Amazon RAG Assistant

A Retrieval-Augmented Generation (RAG) application that answers Amazon-related customer queries using semantic search and a Large Language Model (LLM). The project retrieves the most relevant information from a knowledge base using FAISS and Sentence Transformers before generating an accurate response with Google's FLAN-T5 model.

## Project Overview

Traditional language models generate responses based only on their pre-trained knowledge. In contrast, Retrieval-Augmented Generation (RAG) first retrieves relevant information from a custom knowledge base and then uses that information to generate a more accurate and context-aware answer.

This project demonstrates a basic RAG pipeline using Amazon customer support FAQs as the knowledge base.

---

## Features

- Semantic search using Sentence Transformers
- Fast similarity search with FAISS
- Question answering using Google's FLAN-T5 model
- Retrieval of the most relevant document before answer generation
- Easy to extend with larger datasets or PDF documents
- Built entirely in Google Colab

---

## Technologies Used

- Python
- Google Colab
- Sentence Transformers
- FAISS
- Hugging Face Transformers
- PyTorch
- NumPy

---

## Project Architecture

```
Knowledge Base
       │
       ▼
Sentence Transformer
(Create Embeddings)
       │
       ▼
FAISS Vector Database
       │
       ▼
User Query
       │
       ▼
Query Embedding
       │
       ▼
Retrieve Similar Documents
       │
       ▼
FLAN-T5
       │
       ▼
Generated Answer
```

---

## Workflow

1. Store Amazon-related documents in a knowledge base.
2. Convert each document into vector embeddings using Sentence Transformers.
3. Store the embeddings in a FAISS vector database.
4. Convert the user's question into an embedding.
5. Retrieve the most relevant document using cosine similarity.
6. Pass the retrieved context and question to FLAN-T5.
7. Generate and display the final answer.

---

## Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Amazon-RAG-Assistant.git
```

Move into the project directory

```bash
cd Amazon-RAG-Assistant
```

Install the required libraries

```bash
pip install sentence-transformers
pip install transformers
pip install faiss-cpu
pip install torch
pip install numpy
```

---

## Running the Project

Run the notebook in Google Colab or Jupyter Notebook.

Open

```
Amazon_RAG_Assistant.ipynb
```

Execute each cell sequentially.

---

## Sample Questions

- What is Amazon?
- How can I track my Amazon order?
- What is Amazon Prime?
- How do I return an order?
- How can I cancel an order?
- How do I update my payment method?
- How do I purchase an Amazon gift card?
- How do I contact Amazon customer support?

---

## Sample Output

**Question**

```
What is Amazon?
```

**Retrieved Context**

```
Amazon is a multinational technology and e-commerce company that allows customers to buy products online, stream digital content, use cloud computing services, and access subscription services like Amazon Prime.
```

**Generated Answer**

```
Amazon is a multinational technology company primarily known for its e-commerce platform. It also offers cloud computing services, digital streaming, and subscription services such as Amazon Prime.
```

---

## Folder Structure

```
Amazon-RAG-Assistant/
│
├── Amazon_RAG_Assistant.ipynb
├── README.md
└── requirements.txt
```

---

## Future Improvements

- Support PDF document uploads
- Multiple document retrieval
- Chat interface using Streamlit
- Citation of retrieved sources
- ChromaDB integration
- Hybrid search
- Larger knowledge base
- Conversation memory

---

## Learning Outcomes

Through this project, I gained practical experience with:

- Retrieval-Augmented Generation (RAG)
- Vector databases
- Semantic search
- Embedding models
- Large Language Models (LLMs)
- Hugging Face Transformers
- FAISS indexing
- Prompt engineering

---

## Author

**Bindu Duggisetty**

Integrated M.Tech Software Engineering

VIT-AP University

GitHub: https://github.com/bindusri2605
