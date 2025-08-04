LangChain - Smart Search Chatbot

This is a Streamlit web application that serves as an intelligent chatbot capable of searching the web using various tools powered by LangChain. It provides a conversational interface where users can ask questions, and the underlying AI agent will determine the best approach to find answers, leveraging tools like DuckDuckGo for general web searches, Arxiv for scientific preprints, and Wikipedia for encyclopedic knowledge.

Features

* Conversational AI: Interact with a chatbot that understands your queries.
* Intelligent Agent: Utilizes LangChain's ZERO_SHOT_REACT_DESCRIPTION agent to make informed decisions on which search tool to use.
* Multiple Search Tools: Integrates with:
    * DuckDuckGo Search: For general web queries.
    * Arxiv API: For searching scientific papers and preprints.
    * Wikipedia API: For comprehensive information on various topics.
* Real-time Agent Thoughts: See the agent's thought process and actions unfold in real-time within the Streamlit interface. This offers transparency and insight into how the AI is working.
* Groq Integration: Uses the Groq API for fast inference with the Llama3-8b-8192 model, providing responsive and intelligent replies.

Getting Started

Follow these steps to set up and run the application locally.

Prerequisites

Before you begin, ensure you have the following installed:

* Python 3.8+
* pip (Python package installer)

Installation

1.  Clone the repository (or download abhi.py):
    git clone your-repository-url
    cd your-repository-name # if you cloned a repo

2.  Create a virtual environment (recommended):
    python -m venv venv
    source venv/bin/activate # On Windows: venv\Scripts\activate

3.  Install the required dependencies:
    pip install -r requirements.txt
    (Note: You'll need to create a requirements.txt file. See "Creating requirements.txt" below.)

API Key Setup

This application requires a Groq API key to function.

1.  Get your Groq API Key:
    * Visit the Groq website and sign up or log in.
    * Generate a new API key.

2.  Provide the API Key in the Streamlit App:
    When you run the application, there will be a sidebar where you can input your Groq API key securely.

Running the Application

1.  Start the Streamlit application:
    streamlit run app.py

2.  Access the App:
    Your default web browser should automatically open to the Streamlit application (usually http://localhost:8501).

Configuration

The abhi.py script itself contains some basic configurations:

* Arxiv API Wrapper: top_k_results=1, doc_content_chars_max=200 (can be adjusted for more/less detail).
* Wikipedia API Wrapper: top_k_results=1, doc_content_chars_max=200 (can be adjusted).
* LLM Model: Currently set to Llama3-8b-8192. This can be changed to other Groq-supported models.

requirements.txt

Create a file named requirements.txt in the same directory as app.py with the following content:

streamlit>=1.0.0
langchain-groq
langchain-community
langchain
python-dotenv

* Wikipedia
* DuckDuckGo
```
