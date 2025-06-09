#  Telugu Text Proofreading Platform (OCR-Based)

## Project Overview

This is a **web-based proofreading platform** built specifically for documents in **Telugu**. Users can upload **PDFs or images** that contain Telugu content, and the platform will intelligently extract the text using **Optical Character Recognition (OCR)**. The extracted Telugu text is displayed in an editable format for easy proofreading or further editing.

The system is capable of handling:
- **Selectable/encoded PDFs** (text can be extracted directly)
- **Scanned PDFs or image files** (text is extracted using OCR via Tesseract)

This tool is particularly useful for **digitizing, correcting, or reformatting** Telugu documents.



##  Features

-  Upload **PDF** or **image (JPG, PNG)** files containing Telugu text
-  Automatically detects and extracts Telugu text using **Tesseract OCR**
-  Displays extracted text in an **editable textarea** for proofreading
-  Works for both **encoded PDFs** and **scanned/image-based documents**
-  Clean and minimal user interface



##  Technologies Used

# Frontend
- **HTML, CSS, JavaScript** – For a responsive and interactive user interface

#  Backend
- **Python + Flask** – Handles file uploads, OCR processing, and routing
- **Werkzeug** – Secure file handling and temporary storage

#  Text Extraction
- **PyMuPDF (fitz)** – For extracting text from digitally encoded PDFs
- **Tesseract OCR** (with Telugu language pack) – For scanned documents and images


# Folder Structure

project-root/
│
├── app.py # Main Flask application
├── templates/
│ └── index.html # HTML frontend
├── static/
│ ├── script.js # JavaScript logic (if any)
│ └── style.css # CSS styles
├── uploads/ # Temporary storage for uploaded files
├── requirements.txt # Python dependencies
└── README.md # This file



#  Installation

# 1. Install dependencies
pip install -r requirements.txt

# 2. Install Tesseract OCR and Telugu language pack

# For Ubuntu/Debian
sudo apt install tesseract-ocr tesseract-ocr-tel

# For Windows:
Download Tesseract from https://github.com/tesseract-ocr/tesseract
Install and add the Tesseract path to your system environment variables
Telugu language file usually comes with the installer or can be added manually

# 3. Run the application
python app.py
 Usage
Open your browser and navigate to: http://127.0.0.1:5000/
Upload a PDF or image with Telugu content.

The app will:

Extract directly if text is encoded
Use OCR if it's scanned
The extracted Telugu text will appear in a textarea for proofreading or editing.
Copy or save the corrected Telugu content as needed.

## Future Improvements

 Add download/export option for the edited text
 Add support for spell-check in Telugu
 Enhance OCR for low-quality scans
 Add dark mode and font-size control
 Support bulk document upload
