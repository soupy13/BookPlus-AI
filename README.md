# BookPlus: LLM Semantic Book Recommender 📚

BookPlus is a modern recommendation engine that moves beyond simple keyword matching. By leveraging **Large Language Models (LLMs)** and **Vector Databases**, it understands the "vibe," themes, and emotional resonance of books to provide deeply relevant suggestions based on natural language queries.

---

## 🚀 Key Features

* **Semantic Search:** Describe what you are looking for in plain English (e.g., "a lonely astronaut finding hope" or "dark academia with a twist") rather than just searching by title or author.
* **Vectorized Knowledge:** Uses **OpenAI's `text-embedding-ada-002`** to transform book descriptions into high-dimensional vectors, capturing the nuanced meaning of the text.
* **Intelligent Filtering:** Integrated **Zero-Shot Classification** (BART) to distinguish between Fiction and Non-Fiction and **Sentiment Analysis** (RoBERTa) to filter books by emotional tone (Joy, Sadness, Suspense, etc.).
* **Efficient Retrieval:** Powered by **ChromaDB** (or Weaviate) for lightning-fast approximate nearest neighbor (ANN) searches across thousands of titles.

---

## 🛠️ Tech Stack

| Category | Tools |
| :--- | :--- |
| **Language** | Python 3.9+ |
| **AI/ML Frameworks** | LangChain, Hugging Face Transformers |
| **Embeddings** | OpenAI API |
| **Vector Database** | ChromaDB |
| **Frontend/UI** | Gradio |
| **Data Processing** | Pandas, NumPy |

---

## 📂 Project Structure

```text
├── data/                   # Dataset containing ~7,000 book records
├── notebooks/              # Exploratory Data Analysis & Embedding generation
├── src/
│   ├── recommender.py      # Core logic for semantic search & filtering
│   ├── app.py              # Gradio/Web interface implementation
│   └── database_builder.py # Script to populate the Vector DB
├── requirements.txt        # Project dependencies
└── .env                    # Environment variables (API Keys)
