# RAG_CHATBOT

# 🚀 Overview:

  This project implements a Retrieval-Augmented Generation (RAG) pipeline to enable intelligent question answering over PDF documents. Instead of relying on static responses, the system dynamically retrieves relevant context from documents and generates accurate, human-like answers using open-source language models. 
  The solution is designed to be fully local, cost-free, and scalable, making it ideal for academic use, research experimentation, and production-ready prototypes.

# ✨ Key Highlights:

  📄 Understands and processes unstructured PDF documents
  🔍 Retrieves semantically relevant information using vector search
  🤖 Generates context-aware answers using a lightweight LLM
  💸 No dependency on paid APIs (fully open-source stack)
  ⚡ Fast and efficient retrieval with ChromaDB
  🧩 Modular pipeline (easy to extend and customize)

# 🏗️ System Architecture 
                ┌──────────────┐
                │   PDF Input  │
                └──────┬───────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Text Extraction  │
              └──────┬───────────┘
                     │
                     ▼
              ┌──────────────────┐
              │ Text Chunking    │
              └──────┬───────────┘
                     │
                     ▼
              ┌──────────────────┐
              │ Embeddings       │
              │ (Sentence-BERT)  │
              └──────┬───────────┘
                     │
                     ▼
              ┌──────────────────┐
              │ Vector Database  │
              │ (ChromaDB)       │
              └──────┬───────────┘
                     │
        ┌────────────┴────────────┐
        │                         │
        ▼                         ▼
 User Query               Similarity Search
        │                         │
        └────────────┬────────────┘
                     ▼
              ┌──────────────────┐
              │ Context Retrieval│
              └──────┬───────────┘
                     │
                     ▼
              ┌──────────────────┐
              │ LLM (FLAN-T5)    │
              └──────┬───────────┘
                     ▼
                Final Answer

# 🛠️ Tech Stack :
# Category	       Technology
   Language	          Python
   Framework	          LangChain
   Vector Database        ChromaDB
   Embeddings	          Sentence Transformers
   Language Model  	  FLAN-T5 (Hugging Face)
   Model Hub	          Hugging Face

# 📂 Project Structure   
   rag-pdf-chatbot/
  │
  ├── app.py              # Core application logic
  ├── requirements.txt   # Required libraries
  ├── README.md          # Project documentation

# ⚙️ Installation
  git clone https://github.com/your-username/rag-pdf-chatbot.git
  cd rag-pdf-chatbot 
  
# 🔍 Working Principle :

  - Document Processing: The PDF is loaded and converted into raw text
  - Chunking: Text is divided into smaller segments for better handling
  - Embedding Creation: Each segment is converted into a vector representation
  - Storage: These vectors are stored in ChromaDB for fast access
  - Retrieval: Relevant segments are selected based on the query
  - Response Generation: The selected context is passed to the language model to generate an answer

# ✅ Benefits :
  - Completely free to use (no API cost)
  - Can run locally after initial setup
  - Easy to modify and extend
  - Beginner-friendly implementation of RAG

# 🚀 Future Enhancements :
  - Web-based interface using Streamlit
  - Support for multiple PDFs
  - Chat history and conversational memory
  - Integration with advanced models like Mistral or LLaMA
  - Cloud deployment options

# 📌 Applications :
  - Academic document analysis
  - Knowledge-based Q&A systems
  - Intelligent document assistants
  - Self-learning and study tools

# 📜 License :
   This project is licensed under the MIT License, allowing free use, modification, and distribution.
