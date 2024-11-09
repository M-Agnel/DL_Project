## PDF Querying LLM System
In this project, we developed a PDF querying system using LangChain and a Large Language Model (LLM) to facilitate information extraction from PDF documents through natural language queries. The system allows users to input questions in plain language, and it provides relevant, context-aware responses based on the content within the PDF files. This solution is especially beneficial for quickly obtaining specific information from lengthy documents, such as research papers or reports. By leveraging LangChain's capabilities to process document text and the LLM's ability to interpret complex queries, our system makes document analysis more efficient and accessible.

# Features
Natural Language Querying: Ask questions in natural language, and the system will locate and extract the relevant content from the PDF.
Interactive Responses: The LLM provides responses based on context, ensuring accurate and concise answers.
Efficient Information Retrieval: Reduces the need to manually search through large documents.

# PDF Querying System Using Astra and LangChain
This project demonstrates how to build a PDF querying system using LangChain with a vector search database on Astra DB. The system enables efficient querying of PDF content through natural language, utilizing a combination of LLM embeddings and vector storage for fast and accurate responses to user queries.

# Project Overview
This notebook, titled "Querying PDF With Astra and LangChain," outlines a complete pipeline to extract, embed, and query information from PDF files. It is ideal for scenarios where users need quick answers from extensive PDF documents, such as research papers, reports, and technical documents.

## 1. Introduction and Setup
The project requires a Serverless Cassandra database with Vector Search on Astra DB.
Dependencies include cassio, langchain, openai, and PyPDF2, which are installed early in the notebook.

## 2. PDF Text Extraction
The code uses PdfReader from PyPDF2 to load and read text from a PDF file (e.g., budget_speech.pdf), converting it to a format that can be processed for embedding.

## 3. Database Connection and Initialization
An Astra DB connection is initialized using a secure token.
LangChain embeddings and an OpenAI-based LLM are configured to process and interpret queries.

## 4. Text Splitting and Vector Store Loading
The text extracted from the PDF is split into smaller sections using LangChain’s CharacterTextSplitter.
These sections are then loaded into a vector store backed by Astra DB, allowing for efficient and context-aware information retrieval.

## 5. Query Loop
The notebook provides an interactive loop where users can enter queries in natural language.
LangChain processes each query to retrieve and display relevant responses from the embedded PDF content, providing an intuitive Q&A experience.

## Requirements
Python 3.7+
Astra DB Account with Vector Search enabled
OpenAI API Key for the LLM

## Usage
Place the target PDF file in the project directory.
Run the notebook PDFQuery_LangChain.ipynb.
Enter questions into the input cell as prompted, and retrieve information directly from the PDF content.
