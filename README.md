# Local LLM Webapp for Your Files

> Chat with your own files using open-source Large Language Models!

## Introduction

This project provides a local web application that allows you to interact with your own files using the power of open-source Large Language Models (LLMs).  It leverages Langchain for document processing and chain management, Hugging Face models for embeddings, and Streamlit for a user-friendly interface.  This means your data stays local, and you don't need to rely on external APIs for processing.

## How It Works

The application processes your files (currently supports text files, but can be extended) in the following manner:

1. **File Upload:** You upload your files through the Streamlit interface.

2. **Text Extraction:** The application extracts the text content from the uploaded files.  Future versions will support various file formats.

3. **Text Chunking:**  The extracted text is broken down into smaller, manageable chunks. This is crucial for handling large documents and optimizing LLM performance.

4. **Embedding Generation:** Hugging Face models are used to create vector embeddings for each text chunk. These embeddings capture the semantic meaning of the text.

5. **Local LLM Interaction:** When you ask a question, the application calculates the embedding of your query. It then compares this query embedding to the embeddings of the text chunks to find the most relevant ones.

6. **Contextual Response:** The most relevant chunks, along with your question, are passed to a locally running open-source LLM. The LLM generates a response based on the provided context.

## Dependencies and Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/andrewjohnaj/local-llm-app-for-your-files.git
   ```

2. **Create a Virtual Environment (Recommended):**
   ```bash
   python3 -m venv venv  # Create a virtual environment
   source venv/bin/activate  # Activate the environment (Linux/macOS)
   venv\Scripts\activate  # Activate the environment (Windows)
   ```

3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Run the Streamlit App:**
   streamlit run app.py

2. **Access the Web App:** The application will launch in your web browser.

3. **Upload Files:** Use the file upload feature to add the files you want to chat with.

4. **Ask Questions:**  Type your questions in the chat interface and the LLM will generate responses based on the content of your uploaded files.

## Contributing

Contributions are welcome! Please open issues and pull requests for bug fixes, feature additions, or improvements.

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
