# 🎬 Voice-Based Movie RAG System

## Overview

This project implements a **Voice-Based Retrieval-Augmented Generation (RAG) System** for movie subtitle search. Users can speak a query, which is converted into text using OpenAI Whisper. The system then performs semantic search over a large movie subtitle database and retrieves the most relevant movie dialogues or scenes.

The project combines:

* Speech-to-Text (Whisper)
* Semantic Search
* Sentence Embeddings
* Vector Databases (ChromaDB)
* Movie Subtitle Retrieval

---

## Features

✅ Voice query input using audio files

✅ Speech-to-text conversion using Whisper

✅ Subtitle data preprocessing and cleaning

✅ Text chunking for efficient retrieval

✅ Embedding generation using Sentence Transformers

✅ Vector storage using ChromaDB

✅ Semantic similarity search

✅ Retrieval of relevant movie dialogues and scenes

---

## Tech Stack

### Programming Language

* Python

### Libraries

* Whisper
* Sentence Transformers
* ChromaDB
* Scikit-Learn
* Pandas
* NumPy
* NLTK
* SQLite3
* Torch

### Models

* Whisper Base Model
* intfloat/e5-base-v2 Sentence Transformer

---

## Project Workflow

### 1. Data Loading

Movie subtitle data is loaded from a SQLite database.

### 2. Data Cleaning

Subtitle files are cleaned by removing:

* Timestamps
* Subtitle numbering
* Special characters
* Unwanted formatting

### 3. Document Creation

Subtitles belonging to the same movie are merged into complete documents.

### 4. Text Chunking

Large subtitle documents are split into smaller chunks to improve retrieval performance.

### 5. Embedding Generation

Each chunk is converted into a dense vector representation using:

```python
intfloat/e5-base-v2
```

### 6. Vector Database Storage

Embeddings are stored in ChromaDB for fast similarity search.

### 7. Voice Query Processing

Audio input is converted into text using Whisper.

### 8. Semantic Retrieval

The query embedding is compared with stored subtitle embeddings to retrieve the most relevant movie scenes.

---

## Example Query

Voice Input:

```text
He is hiding something from the family
```

Retrieved Output:

```text
Most semantically relevant movie subtitle chunks related to the query.
```

---

## Folder Structure

```text
Voice_Based_Movie_RAG/
│
├── Voice_Based_Movie_RAG.ipynb
├── README.md
├── requirements.txt
└── subtitle_database.db
```

---

## Installation

Clone the repository:

```bash
git clone <your-repository-link>
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Future Improvements

* Real-time microphone input
* RAG response generation using LLMs
* Streamlit web application
* Movie recommendation integration
* Faster vector retrieval optimization

---

## Learning Outcomes

Through this project I learned:

* Retrieval-Augmented Generation (RAG)
* Vector Databases
* Semantic Search
* Sentence Embeddings
* Speech Recognition
* Whisper Model Integration
* ChromaDB Implementation
* NLP Pipeline Development

---

## Author

Zaiba Ansari

Aspiring Data Scientist | Machine Learning Enthusiast | NLP Projects
