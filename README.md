# Electrochemistry Assistant

This project is a question-answering system focused on electrochemistry. It uses Google's Gemini model and a vector database (ChromaDB) to find relevant information from PDF documents and provide helpful answers to your questions about electrochemistry.

[![Kaggle](https://kaggle.com/static/images/open-in-kaggle.svg)](https://www.kaggle.com/code/aravindannatarajan/electrochemistry-assistant-v2)

### Workflow

1.  **Document Processing:** Extracts text from PDF documents related to electrochemistry using `pdfminer.six`.
2.  **Embedding Generation:** Creates embeddings for the extracted text using the Gemini API and stores them in a ChromaDB vector database.
3.  **Query Processing:** Generates embeddings for user queries using the Gemini API.
4.  **Retrieval:** Searches the vector database for relevant documents based on the query embeddings using TF-IDF, BM25, and Gemini models.
5.  **Evaluation:** Evaluates the performance of the retrieval using metrics like Accuracy, Precision, Recall, F1-score, MRR, P@K, and NDCG@K.
6.  **Answer Generation:** Uses the Gemini model with a prompt enriched by the retrieved documents to answer the user's question in a comprehensive and user-friendly way.
7.  **Semantic Similarity Evaluation:** Assesses the quality and relevance of the generated answer by comparing it to the retrieved passages using a pre-trained Sentence Transformer model and calculating semantic similarity scores.

### Gen AI Features

*   **Embeddings:** Used to represent documents and queries as vectors, enabling semantic search for relevant information.
*   **Retrieval Augmented Generation (RAG):** Retrieves relevant context from the document database to enhance the answer quality and accuracy.
*   **Document understanding:** Allows the system to process and understand information from PDF documents containing electrochemical knowledge.
*   **Large Language Models:** Utilizes the powerful Gemini model for accurate comprehension, generation, and contextualization of natural language.

## Prerequisites

*   Python 3.7 or higher
*   Access to Google Colab or a Jupyter Notebook environment or a Kaggle environment
*   A Google Cloud API key with access to the Gemini API.

## Setup

1.  Clone this repository.
2.  Install the required libraries:
```pip install -qU "google-genai==1.7.0" "chromadb==0.6.3" "pdfminer.six" "hf_xet" "rank_bm25" sentence-transformers==2.2.2```
3. Set up your Google Cloud API key for the Gemini API. If using Kaggle, add it as a secret named "GOOGLE_API_KEY". Otherwise, load it securely as an environment variable.
4.  The project will automatically download the electrochemistry PDF data from Kaggle.

## API Key Authentication

You need to securely provide your Google API key. If you are using Kaggle, follow these steps:

1.  Go to the "Add-ons" menu.
2.  Select "Secrets".
3.  Add a new secret named "GOOGLE_API_KEY" and paste your Google Cloud API key as the value.

If you are not using Kaggle, you will need to find an alternative secure method to load your API key as an environment variable.

Please refer to [this](https://www.kaggle.com/code/markishere/day-1-prompting#Day-1---Prompting) notebook for detailed setup instructions.

## Dataset

The documents used for this project are PDF files related to electrochemistry techniques, stored in the `data` folder. You can download the dataset from Kaggle [here](https://www.kaggle.com/code/aravindannatarajan/electrochemistry-assistant-v2)

## Potential Applications

* **Educational tool:** Aids in learning electrochemical principles.
* **Research assistant:** Assists in exploring electrochemical literature.
* **Customer support chatbot:** Answers questions about electrochemical products or services.

## Contributing

Contributions are welcome! Please feel free to open issues or pull requests for any improvements or bug fixes.

## Versioning
The notebooks and the repositories are versioned using [SemVer(https://semver.org/)] for versioning. The current version is 2.0.

## License

This project is licensed under the [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.en).

## Author
Aravindan Natarajan