# Electrochemistry Assistant - My First RAG

This project showcases a question-answering system for electrochemistry, built using Google's Gemini model, ChromaDB, and Retrieval Augmented Generation (RAG). This is the capstone project developed for the Kaggle's 5 day Gen AI Intesive course with Google. 

[![Kaggle](https://kaggle.com/static/images/open-in-kaggle.svg)](https://www.kaggle.com/code/aravindannatarajan/electrochemistry-assistant)

## Project Overview

This system efficiently retrieves relevant information from PDF documents to provide comprehensive and user-friendly answers to user queries related to electrochemistry. It was inspired by my participation in Kaggle's 5-day Gen AI intensive workshop, which equipped me with the knowledge and skills to embark on this exciting project.

## How it Works

1. **Document Processing:** Text is extracted from PDF documents related to electrochemistry using `pdfminer`.

2. **Embedding Generation:** Embeddings are created for the extracted text using the Gemini API and stored in a ChromaDB vector database.

3. **Query Processing:** Embeddings are generated for user queries using the Gemini API.

4. **Retrieval:** The vector database searches for relevant documents based on the query embeddings.

5. **Answer Generation:** The Gemini model, enriched with the retrieved documents, generates a comprehensive and user-friendly answer.

## Gen AI Features

* **Embeddings:** Represent documents and queries as vectors for semantic search.
* **Retrieval Augmented Generation (RAG):** Retrieves relevant context to enhance answer quality.
* **Large Language Model (LLM) Capabilities:** Leverages the Gemini model's advanced language understanding and generation abilities.

## Setup and Usage

Please refer to the notebook for detailed setup instructions.

## Dataset

The documents used for this project are PDF files related to electrochemistry techniques, stored in the `capstone-data-pdf` dataset folder. You can download the dataset from Kaggle [here](https://www.kaggle.com/code/aravindannatarajan/electrochemistry-assistant)

## Potential Applications

* **Educational tool:** Aids in learning electrochemical principles.
* **Research assistant:** Assists in exploring electrochemical literature.
* **Customer support chatbot:** Answers questions about electrochemical products or services.

## Contributing

Contributions are welcome! Please feel free to open issues or pull requests for any improvements or bug fixes.

## License

This project is licensed under the [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.en).

## Author
Aravindan Natarajan

## Acknowledgments

* Prof. Richard.S.Kelly for creating the valuable electrochemical resources used in this project. [Analytical Electrochemistry: The Basic Concepts](https://www.asdlib.org/onlineArticles/ecourseware/Kelly_Potentiometry/EC_CONCEPTS1.HTM)
* Google AI for developing the Gemini model.
* ChromaDB for providing the vector database.
* Kaggle for hosting the Gen AI intensive workshop.
