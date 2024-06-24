## PDFs Chat App

# Introduction

The MultiPDF Chat App is a Python-based application designed to interact with multiple PDF documents. It allows users to ask questions in natural language, and the app responds with relevant information extracted from the PDFs. Leveraging a language model, the app provides accurate answers related to the content of the loaded documents.


# How It Works

![MultiPDF Chat App Diagram](./docs/PDF-LangChain.jpg)

The app operates through the following steps:

1. **PDF Loading:** The application reads and extracts text from multiple PDF files.
2. **Text Chunking:** The extracted text is divided into manageable chunks for efficient processing.
3. **Language Model:** Utilizing a language model, the app generates vector representations (embeddings) of the text chunks. It employs OpenAI and Hugging Face models, with Streamlit as the front-end.
4. **Similarity Matching:** Upon receiving a question, the app matches it against the text chunks to find the most semantically similar content.
5. **Response Generation:** The selected chunks are processed by the language model to generate a response based on the PDF content. The PDFs can be up to 2000MB each, and the app supports multiple PDFs on various topics. Accurate responses are enhanced by using prompt patterns such as Persona, Flipped Interaction, Cognitive Verifier, Template, Chain of Thought, etc.

# Dependencies and Installation

To install the MultiPDF Chat App, follow these steps:

1. Clone the repository to your local machine.
2. Install the necessary dependencies present in requirements.txt

# Acquire an API key from OpenAI and add it to the .env file in the project directory:
OPENAI_API_KEY=your_secret_api_key
HUGGING_FACE_KEY=your_hugging_face_key

# Usage
Run the app.py file using Google Colab. Execute the following commands:
# Install Streamlit
!pip install streamlit
!pip install streamlit -q
!pip install rdkit-pypi

# Run the application
!wget -q -O - ipv4.icanhazip.com
# This will return an IP address, e.g., 35.147.138.250
!streamlit run app.py & npx localtunnel --port 8501
# Click on the provided link to access the app
streamlit run app.py
The app will open in your default web browser with the user interface.
Load multiple PDF documents as instructed.
Ask questions about the loaded PDFs using the chat interface.

# License
The MultiPDF Chat App is distributed under the MIT License.

# Link to the video
https://drive.google.com/file/d/1lKURE8OsVru6vOoCembDeNI3FXtyIwLN/view?usp=sharing

