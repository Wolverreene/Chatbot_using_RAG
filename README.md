# Chatbot using RAG

This project is a domain-specific chatbot built for the **School of Interdisciplinary Engineering & Sciences (SINES)** at **NUST**. It leverages **Retrieval-Augmented Generation (RAG)** with OpenAI’s **GPT-3.5 Turbo** as the Large Language Model (LLM), and is designed to assist students, faculty, and visitors by answering queries about SINES using officially sourced and manually collected data.

---

## Features

- **Custom Knowledge Base** from:
  - Official SINES website (web crawling)
  - Manually collected data via **Google Forms** (lab functions, ongoing research, equipment)
  - Physical **mapping of department building** (labs, offices, restrooms, extinguishers, etc.)
- **RAG-based Retrieval Pipeline** to fetch accurate context from documents
- **GPT-3.5 Turbo Integration** via API for natural language responses
- **Interactive UI** built using [Panel](https://panel.holoviz.org/) for smooth user experience
- **Multiple RAG Chain Modes**: `stuff`, `map_reduce`, `refine`, `map_rerank`

- ## How to Run

### Prerequisites

- Python 3.8+
- OpenAI account with access to API key
- Internet connection
- Install the required library:

```bash
!pip install langchain
```

### Steps to Run

1. Open the Notebook: 'ChatbotNLP.ipynb'
2. Set your OpenAI API Key:

    Replace the placeholder in the notebook with your API key:
```bash
params[variable] = params.get(variable, os.environ.get(variable, "placeholder"))
```
3. Run the Web App:
4. Open Anaconda Prompt or Python terminal and run:
```bash
panel serve chatbotNLP.ipynb
```
5. Access the Chatbot:
  Copy the URL shown in the terminal (e.g., http://localhost:5006/ChatbotNLP) and open it in a browser.


Tested on Windows OS. Compatibility with other operating systems may require adjustments.


## Results
Screenshots of interface:
1. General Query
2. Contact Info


## Technology Used

- OpenAI GPT-3.5 Turbo
- LangChain
- Panel (for UI)
- PDF Text Extraction & Chunking
- Manual and Automated Data Collection

## Use Cases

- Students exploring research labs or projects
- Faculty contact and departmental directory lookup
- Visitors navigating the department building
- Admins quickly answering common questions

## Notes

- The OpenAI API key used during development has been excluded for security.
- You must insert your own API key as described above.
- The project was tested and confirmed to work on Windows OS.
