

# Document Conversion and Chatbot with Streamlit

This project is a **Streamlit** web application that provides document conversion features (PDF, text, Word, and images) and a chatbot interface to interact with the extracted text using **Google's Gemini Generative AI** model. It supports Optical Character Recognition (OCR) using **Tesseract**, file conversions, and user-friendly downloads of text in various formats like PDF, JPEG, and Word documents.

## Features

- **File Upload Support**: Upload an image (`.jpg`, `.jpeg`, `.png`), PDF, plain text, or Word document (`.docx`).

- **Text Extraction**: Extract text from PDFs, images, and Word documents using Tesseract and pdfplumber.

- **File Conversion**:
  - Text files can be converted to PDF, JPEG, and Word documents.
  - PDFs can be converted to text and Word documents.
  - Images can be converted to text, PDFs, and Word documents.
  - Word documents can be converted to PDFs.

- **Chatbot Interaction**: After text extraction, users can ask questions based on the extracted content, and the **Gemini Generative AI** will provide answers. 
  - **Download Option for Responses**: Users can download the chatbot's responses as a PDF file for easy reference.

- **Download Options**: After extraction or conversion, the resulting text can be downloaded in multiple formats (PDF, Word, JPEG, etc.).

## Tech Stack

- **Streamlit**: For the web interface.
- **Tesseract**: For OCR to extract text from images.
- **pdfplumber**: For extracting text from PDFs.
- **Google Generative AI (Gemini)**: Used for interactive chatbot responses.
- **PIL (Pillow)**: For image processing.
- **ReportLab**: For generating PDFs from text.
- **Python-dotenv**: For managing environment variables.

## Requirements

1. Python 3.x
2. **Tesseract OCR**: Ensure Tesseract is installed and the path to the executable is correctly configured in the script.

### Python Libraries:
- streamlit
- pdfplumber
- pytesseract
- Pillow (PIL)
- google-generativeai
- python-docx
- reportlab
- python-dotenv

### NLTK Data (optional for extra processing):
- punkt
- wordnet
- stopwords

## Setup

1. Clone the repository.
   ```bash
   git clone https://github.com/your-repo/document-chatbot.git
   cd document-chatbot
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Install **Tesseract OCR**:
   - Download and install Tesseract from [here](https://github.com/tesseract-ocr/tesseract).
   - Set the Tesseract path in your script:
     ```python
     pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
     ```

4. Set up the **Gemini API**:
   - Create a `.env` file in the root directory.
   - Add your Google API key to the `.env` file:
     ```plaintext
     API_KEY=your-google-api-key
     ```

## Usage

1. Run the Streamlit app:
   ```bash
   streamlit run app.py
   ```

2. Upload a file (PDF, image, text, or Word document).

3. Extract and view the text from the uploaded file.

4. Download the converted text in your preferred format.

5. Use the chatbot feature to ask questions based on the extracted text. You can also download the chatbot's responses for future reference.

## Example

### Uploading a PDF
- The PDF will be processed to extract text using **pdfplumber**.
- You can download the extracted text as a `.txt` file, convert it to Word, or convert it to JPEG format.
- You can also ask the chatbot questions about the text using **Google's Gemini AI**.

### Uploading an Image
- The image is processed through **Tesseract OCR** to extract text.
- You can download the extracted text in text, PDF, or Word formats.

### Chatbot Interaction
- Enter a question in the text input box.
- The chatbot uses the extracted text to generate a response via **Gemini AI**.
- **Download Chatbot Response**: After the chatbot responds, you can download the answer as a PDF for easy reference.

## Notes
- Ensure that **Tesseract** is properly installed and the path is correctly set in the script.
- Ensure you have the correct **Google Gemini AI** API key set in your environment variables.

---
