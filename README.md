# financial-web-analyzer
# AI Financial Advisor using Retrieval-Augmented Generation (RAG)

## Overview

AI Financial Advisor is a Retrieval-Augmented Generation (RAG) application that enables users to upload one or more company financial reports (PDFs) and receive intelligent, document-grounded financial analysis.

Instead of relying on the language model's pre-trained knowledge, the application retrieves relevant information from the uploaded reports using semantic search and generates answers based only on those retrieved sections. This helps reduce hallucinations and ensures that investment insights are supported by evidence from the uploaded documents.

The application can analyze annual reports, 10-K filings, earnings reports, balance sheets, income statements, and other financial documents.

---

## Features

* Upload one or multiple financial report PDFs
* Automatic PDF text extraction
* Intelligent document chunking
* Semantic search using Mistral Embeddings
* Chroma Vector Database
* MMR (Maximum Marginal Relevance) Retrieval
* Interactive AI chat interface
* Investment recommendation (Strong Buy / Buy / Hold / Sell / Strong Sell)
* Revenue analysis
* Profitability analysis
* Debt analysis
* Cash flow analysis
* Business risk analysis
* Future outlook analysis
* Source-backed responses with page citations
* Modern Streamlit web interface

---

## Tech Stack

### Frontend

* Streamlit

### Backend

* Python
* LangChain

### Vector Database

* ChromaDB

### Embedding Model

* Mistral AI Embeddings

### Large Language Model

* Mistral Small

### Document Processing

* PyPDFLoader
* RecursiveCharacterTextSplitter

### Environment Management

* python-dotenv

---

## System Architecture

```text
                     Company Financial Report (PDF)
                                  │
                           PyPDFLoader
                                  │
                  RecursiveCharacterTextSplitter
                                  │
                       Mistral AI Embeddings
                                  │
                             ChromaDB
                                  │
                         MMR Retriever
                                  │
                     Relevant Financial Chunks
                                  │
                    Financial Advisor Prompt
                                  │
                          Mistral Small LLM
                                  │
         Financial Analysis + Investment Recommendation
```

---

## Workflow

1. Upload one or more company financial reports.
2. Extract text from each PDF.
3. Split documents into overlapping chunks.
4. Generate vector embeddings using Mistral AI.
5. Store embeddings in ChromaDB.
6. User asks a financial question.
7. Relevant document chunks are retrieved using semantic search.
8. Retrieved context is sent to the Mistral language model.
9. The AI generates an answer using only the retrieved information.
10. The application displays the answer along with supporting document excerpts.

---

## Example Questions

* Summarize this company.
* Should I invest in this company?
* Analyze the company's revenue growth.
* Analyze profitability.
* Analyze cash flow.
* What are the company's major risks?
* What is the debt position?
* What are the strengths and weaknesses?
* What is the future outlook?
* Compare this company with another uploaded company.

---

## Project Structure

```text
financial-web-analyzer/
│
├── app.py
├── requirements.txt
├── .env
├── README.md
├── chroma_db/
└── assets/
```

---

## Installation

Clone the repository

```bash
git clone https://github.com/your-username/financial-web-analyzer.git
cd financial-web-analyzer
```

Create a virtual environment

```bash
python -m venv .venv
```

Activate the environment

Windows

```bash
.venv\Scripts\activate
```

Linux/macOS

```bash
source .venv/bin/activate
```

Install dependencies

```bash
pip install -r requirements.txt
```

Create a `.env` file

```env
MISTRAL_API_KEY=your_mistral_api_key
```

Run the application

```bash
streamlit run app.py
```

---

## How It Works

The application follows the Retrieval-Augmented Generation (RAG) pipeline:

* Financial reports are uploaded by the user.
* Text is extracted from PDFs.
* Documents are split into overlapping chunks.
* Chunks are converted into vector embeddings.
* Embeddings are stored inside ChromaDB.
* User queries retrieve the most relevant chunks.
* Retrieved context is passed to the Mistral language model.
* Responses are generated only from the retrieved document context.

This approach improves factual accuracy and reduces hallucinations.

---

## Applications

* Investment research
* Equity research
* Financial statement analysis
* Company report summarization
* Financial education
* Business intelligence
* Portfolio research

---

## Future Improvements

* Multi-company comparison
* Financial ratio calculations
* Live stock market integration
* SEC filing support
* Interactive charts and visualizations
* Downloadable PDF investment reports
* Conversation memory
* Hybrid retrieval (semantic + keyword)
* Portfolio recommendation engine
* Support for quarterly earnings reports

---

## Screenshots

Add screenshots of:

* Upload page
* Chat interface
* Investment recommendation
* Retrieved document citations

---

## Author

**Aditya Gupta**

B.Tech – Data Science

---

## License

This project is licensed under the MIT License.

