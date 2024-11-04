# PDF Querying Chatbot with Falcon LLMs

This project builds a customizable, private PDF chatbot that uses **Falcon-7B** and **Falcon-40B** Large Language Models (LLMs) to answer queries on PDF content. Unlike other implementations, this bot provides end-to-end control over preprocessing, ranking, and retrieval of results, ensuring that your data remains private and that you have flexibility over each step of the bot's operations.

## Key Features

- **End-to-End Control**: Configure each aspect of the chatbot, from text extraction to model parameters and search tuning.
- **Natural Language Querying**: Seamlessly query PDF documents using natural language, with responses tuned to be helpful, accurate, and contextually aware.
- **Privacy-Focused Processing**: No third-party services are required for handling PDFs; data remains private and is processed locally.
- **Dual-Model Support**: Provides options for **Falcon-7B** and **Falcon-40B** models, allowing different levels of response sophistication.
- **Advanced Search and Ranking**: Combines semantic and cross-encoder search techniques to deliver the most relevant results from PDF content.

## Tech Stack

- **Programming Language**: Python 3.8+
- **LLMs**: Falcon-7B and Falcon-40B, hosted via custom `Client` endpoints.
- **PDF Processing**: `pdfminer` for robust PDF text extraction.
- **Semantic Search and Ranking**: `sentence-transformers` and `CrossEncoder` models from Hugging Face for semantic search and relevance scoring.

## Getting Started

### Prerequisites

1. Install Python 3.8 or higher.
2. Set up a virtual environment:
   ```bash
   python3 -m venv env
   source env/bin/activate  # On Windows use `env\Scripts\activate`
