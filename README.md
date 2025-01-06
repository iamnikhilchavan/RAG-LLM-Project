
# RAG-LLM Project

A Streamlit application leveraging LangChain and Retrieval-Augmented Generation (RAG) for extracting and analyzing information from research papers and other documents. This project demonstrates how to integrate state-of-the-art language models with document retrieval and vector storage for efficient data processing.

---

## Features

- **Document Parsing**: Extract information from PDF research papers.
- **LangChain Integration**: Utilize LangChain for text splitting, embedding, and query processing.
- **Vector Storage**: Implement a Chroma vector store for storing and retrieving document embeddings.
- **Streamlit Frontend**: Interactive user interface to upload documents, perform queries, and visualize results.
- **Dockerized Deployment**: Run the entire application in a Docker container for seamless deployment.

---

## Project Structure

```
RAG-LLM/
├── App/
│   ├── db/                      # Database folder
│   ├── dockerfile               # Dockerfile for containerization
│   ├── functions.py             # Core utility functions
│   ├── requirements.txt         # Python dependencies
│   ├── streamlit_app.py         # Streamlit application code
├── Data/
│   ├── langchain-retrieval-augmented...pdf # Sample research paper
│   ├── NIPS-2017-attention-is-all-you-need.pdf # Another research paper
├── myenv/                      # Local Python environment (ignored by Git)
├── Vectorstore/                # Vector database files (ignored by Git)
├── vectorstore_chroma/         # Chroma-specific vector storage
├── .env                        # Environment variables file (ignored by Git)
├── .gitignore                  # Ignored files for Git
├── data_extraction_llms.ipynb  # Jupyter Notebook for experimentation
```

---

## Prerequisites

- **Python**: Version 3.11
- **Docker**: Installed and running
- **Git**: Installed for version control
- **OpenAI API Key**: Required for interacting with the GPT models

---

## Installation

### Option 1: Run Locally
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/RAG-LLM-Project.git
   cd RAG-LLM-Project
   ```

2. Create a virtual environment:
   ```bash
   python3 -m venv myenv
   source myenv/bin/activate  # For Linux/Mac
   myenv\Scripts\activate     # For Windows
   ```

3. Install dependencies:
   ```bash
   pip install --no-cache-dir -r requirements.txt
   ```

4. Run the Streamlit app:
   ```bash
   streamlit run App/streamlit_app.py
   ```

### Option 2: Run with Docker
1. Build the Docker image:
   ```bash
   docker build -t streamlit-app .
   ```

2. Run the Docker container:
   ```bash
   docker run -p 8501:8501 streamlit-app
   ```

3. Access the app at: [http://localhost:8501](http://localhost:8501)

---

## How It Works

1. **Upload Documents**: Drag and drop research papers in the Streamlit interface.
2. **Query Processing**: Ask questions or enter search terms.
3. **RAG Workflow**:
   - Splits the document into smaller chunks.
   - Generates embeddings for each chunk using LangChain.
   - Stores embeddings in a Chroma vector store.
   - Retrieves relevant chunks based on user queries.
4. **Interactive Results**: View answers, sources, and reasoning in an easy-to-read format.

---

## Technologies Used

- **LangChain**: Document splitting, embeddings, and RAG workflow.
- **Streamlit**: For building an interactive frontend.
- **Chroma Vector Store**: Efficient storage and retrieval of document embeddings.
- **Docker**: Containerized deployment for seamless execution.

---

## Future Enhancements

- Add support for additional document types (e.g., Word, TXT).
- Improve query answering with advanced GPT models.
- Enhance UI/UX with better visualization and analytics.
- Include more sample datasets for testing.

---

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your improvements.

---

## Acknowledgments

- [LangChain](https://github.com/hwchase17/langchain) for providing excellent tools for retrieval-augmented generation.
- [Streamlit](https://streamlit.io/) for simplifying interactive app creation.
- [OpenAI](https://openai.com/) for cutting-edge language models.

---

Feel free to use this project as a template for your own RAG-based applications!
```
