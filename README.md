<h1>PDF Extraction and Q&A using Google Generative AI and Streamlit</h1>
**Overview**
This repository contains a Streamlit application that allows users to upload PDF files, extract text from them, and ask questions based on the content. The application leverages Google Generative AI for embeddings and FAISS for efficient similarity search. Users can interactively ask questions about the uploaded PDF files, and the application will provide detailed answers.

**Features**
Upload multiple PDF files
Extract text from the uploaded PDFs
Split extracted text into manageable chunks
Create a vector store for efficient similarity search
Ask questions and get detailed answers using Google Generative AI
**Prerequisites**
Python 3.7 or higher
Streamlit
PyPDF2
LangChain
FAISS
Google Generative AI SDK
dotenv
**Installation**
Clone the repository:
bash
Copy code
git clone https://github.com/yourusername/pdf-extraction-qa.git
cd pdf-extraction-qa
Create and activate a virtual environment:
bash
Copy code
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
Install the required packages:
bash
Copy code
pip install -r requirements.txt
Set up your Google API Key:
Create a .env file in the project root directory and add your Google API key:

makefile
Copy code
GOOGLE_API_KEY=your_google_api_key
Usage
Run the Streamlit application:
bash
Copy code
streamlit run app.py
Open your web browser and navigate to http://localhost:8501.

In the sidebar, upload your PDF files and click on the "Submit & Process" button. The application will extract and process the text from the PDFs.

Enter your question in the input box and get detailed answers based on the PDF content.

**Code Overview**
Main Functions
get_pdf_text(pdf_docs): Extracts text from uploaded PDF files.
get_text_chunks(text): Splits the extracted text into smaller chunks.
get_vector_store(text_chunks): Creates a vector store using FAISS from text chunks.
get_conversational_chain(): Loads the QA chain with the Google Generative AI model.
user_input(user_question): Handles user questions and retrieves relevant answers from the processed PDF content.
Streamlit Interface
The main interface includes a text input for questions and a sidebar for uploading PDF files.
The "Submit & Process" button triggers the text extraction and processing.
The application displays answers to user questions interactively.

Contact
For any questions or inquiries, please contact ananadparna1203@gmail.com.
