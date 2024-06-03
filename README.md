<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PDF Extraction and Q&A using Google Generative AI and Streamlit</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
            background-color: #f4f4f4;
        }
        h1, h2, h3 {
            color: #333;
        }
        pre {
            background-color: #eee;
            padding: 10px;
            border-radius: 5px;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>PDF Extraction and Q&A using Google Generative AI and Streamlit</h1>
        
        <h2>Overview</h2>
        <p>
            This repository contains a Streamlit application that allows users to upload PDF files, extract text from them, and ask questions based on the content. The application leverages Google Generative AI for embeddings and FAISS for efficient similarity search. Users can interactively ask questions about the uploaded PDF files, and the application will provide detailed answers.
        </p>
        
        <h2>Features</h2>
        <ul>
            <li>Upload multiple PDF files</li>
            <li>Extract text from the uploaded PDFs</li>
            <li>Split extracted text into manageable chunks</li>
            <li>Create a vector store for efficient similarity search</li>
            <li>Ask questions and get detailed answers using Google Generative AI</li>
        </ul>
        
        <h2>Prerequisites</h2>
        <ul>
            <li>Python 3.7 or higher</li>
            <li>Streamlit</li>
            <li>PyPDF2</li>
            <li>LangChain</li>
            <li>FAISS</li>
            <li>Google Generative AI SDK</li>
            <li>dotenv</li>
        </ul>
        
        <h2>Installation</h2>
        <p>1. Clone the repository:</p>
        <pre><code>git clone https://github.com/anandaparna126/Invoice_extraction_using_gemini_pro-pdfs-.git
cd Invoice_extraction_using_gemini_pro-pdfs-
</code></pre>
        
        <p>2. Create and activate a virtual environment:</p>
        <pre><code>python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
</code></pre>
        
        <p>3. Install the required packages:</p>
        <pre><code>pip install -r requirements.txt
</code></pre>
        
        <p>4. Set up your Google API Key:</p>
        <p>Create a <code>.env</code> file in the project root directory and add your Google API key:</p>
        <pre><code>GOOGLE_API_KEY=your_google_api_key
</code></pre>
        
        <h2>Usage</h2>
        <p>1. Run the Streamlit application:</p>
        <pre><code>streamlit run app.py
</code></pre>
        
        <p>2. Open your web browser and navigate to <code>http://localhost:8501</code>.</p>
        
        <p>3. In the sidebar, upload your PDF files and click on the "Submit & Process" button. The application will extract and process the text from the PDFs.</p>
        
        <p>4. Enter your question in the input box and get detailed answers based on the PDF content.</p>
        
        <h2>Code Overview</h2>
        <h3>Main Functions</h3>
        <ul>
            <li><code>get_pdf_text(pdf_docs)</code>: Extracts text from uploaded PDF files.</li>
            <li><code>get_text_chunks(text)</code>: Splits the extracted text into smaller chunks.</li>
            <li><code>get_vector_store(text_chunks)</code>: Creates a vector store using FAISS from text chunks.</li>
            <li><code>get_conversational_chain()</code>: Loads the QA chain with the Google Generative AI model.</li>
            <li><code>user_input(user_question)</code>: Handles user questions and retrieves relevant answers from the processed PDF content.</li>
        </ul>
        
        <h3>Streamlit Interface</h3>
        <ul>
            <li>The main interface includes a text input for questions and a sidebar for uploading PDF files.</li>
            <li>The "Submit & Process" button triggers the text extraction and processing.</li>
            <li>The application displays answers to user questions interactively.</li>
        </ul>
        
        <h2>Contact</h2>
        <p>For any questions or inquiries, please contact <a href="mailto:ananadparna1203@gmail.com">ananadparna1203@gmail.com</a>.</p>
    </div>
</body>
</html>
