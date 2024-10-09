# 📚 Chat with PDF using Gemini AI 🤖

An interactive web application that allows users to upload and chat with multiple PDF documents using Google's Gemini AI. This tool provides seamless querying of PDFs by generating intelligent, context-based responses to user questions.

## 🚀 Project Overview

This project is designed to enable users to interactively extract and query information from PDF documents by leveraging natural language processing (NLP) models and vector search. It processes PDFs into searchable chunks, indexes the text, and allows users to ask questions about the content, with responses provided by Gemini AI.

### 🔍 Key Features:
- **Multi-PDF Upload**: Supports uploading multiple PDF files for simultaneous processing.
- **Natural Language Querying**: Ask questions about the content of the PDFs in natural language.
- **AI-Powered Responses**: Get detailed, context-driven responses using Gemini AI.
- **Efficient Search**: Uses FAISS for fast and accurate similarity search through the indexed PDF content.
- **Simple UI**: Built with Streamlit for an intuitive user experience.

---

## 🛠️ Tech Stack

- **Python**: Backend programming language.
- **Streamlit**: Web framework for building the user interface.
- **PyPDF2**: Library for extracting text from PDF files.
- **LangChain**: NLP library for splitting and embedding text into chunks.
- **FAISS**: Facebook AI's library for vector similarity search.
- **Google Generative AI (Gemini)**: AI model used to generate answers based on user queries.

---

## 🔧 Setup and Installation

### Prerequisites

Before running the application, make sure you have the following installed:

- Python 3.8 or above
- API Key for **Google Generative AI (Gemini)**

### Installation Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/chat-pdf-gemini.git
   cd chat-pdf-gemini
   ```

2. **Install Required Dependencies**
   You can install the required libraries using `pip`:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up Your Google API Key**
   - Obtain your API key from [Google Generative AI](https://developers.generativeai.google/) and add it to your environment.
   - Open the project folder and replace `"YOUR_GEMINI_API_KEY"` with your actual API key in the code.

4. **Run the Application**
   ```bash
   streamlit run app.py
   ```

5. **Open the Application in Your Browser**
   After running the above command, Streamlit will launch the app locally. Open your browser and go to:
   ```
   http://localhost:8501
   ```

---

## 💻 Usage Instructions

1. **Upload PDFs**: 
   - Go to the sidebar and upload your PDF documents by clicking on the **Upload** button.
   
2. **Process PDFs**:
   - After uploading the files, click **Submit & Process** to extract and index the text from the PDFs. This might take a few seconds, depending on the file size.

3. **Ask a Question**:
   - Once the PDFs are processed, you can ask any question about the content of the documents. The AI will respond based on the context extracted from the files.

---

## Project Structure

- `app.py`: The main Python script that runs the Streamlit app.
- `requirements.txt`: Contains the list of dependencies required for the project.
- `faiss_index/`: Directory where the FAISS vector index is stored.
- `README.md`: This file, which provides an overview of the project.

---

## 🧠 How It Works

1. **PDF Text Extraction**: The `PyPDF2` library is used to extract text from each PDF page.
   
2. **Text Chunking**: Text is split into chunks using `LangChain`'s `RecursiveCharacterTextSplitter` to handle large documents effectively. This allows each chunk to be queried individually.

3. **Vector Store Creation**: FAISS is used to create a vector index of the text chunks. This allows for efficient similarity searching when answering questions.

4. **Conversational AI**: Google Gemini AI handles question-answering by generating detailed responses based on the context retrieved from the PDF text.

---

## ✨ Features to Add

- **Support for More File Formats**: Expanding the app to handle DOCX, TXT, and other file formats.
- **Improved UI/UX**: Further enhancements in the design and user experience of the Streamlit interface.
- **Additional AI Models**: Allow the user to choose from different AI models for answering queries.

---

## 🏗️ Contributing

Contributions are welcome! If you'd like to contribute to the project, feel free to submit a pull request or create an issue to discuss potential improvements or bug fixes.

### Steps to Contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -m 'Add new feature'`).
4. Push the changes (`git push origin feature-branch`).
5. Open a Pull Request and describe the changes.

---

## 💬 Contact

If you have any questions or want to discuss the project, feel free to reach out:

- **LinkedIn**: [Hammad Ali](https://www.linkedin.com/in/hammadali1805)
- **GitHub**: [github.com/hammadali1805](https://github.com/hammadali1805)

---

Enjoy chatting with your PDFs! 😄📚
