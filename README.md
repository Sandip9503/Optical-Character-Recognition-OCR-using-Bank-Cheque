🏦 Optical Character Recognition (OCR) using Bank Cheque
This project demonstrates the application of Optical Character Recognition (OCR) to extract textual information from scanned bank cheques. It leverages powerful OCR libraries to detect and process handwritten or printed text, with a focus on extracting critical information such as account number, date, amount, and IFSC code.

📘 Project Overview

Notebook: Bank Cheque OCR.ipynb
Goal: Automatically extract structured text data from cheque images
Use Case: Financial document automation, cheque clearing systems

🧰 Technologies & Libraries Used

Python
OpenCV – Image preprocessing and manipulation
Tesseract OCR – Text recognition engine
Pytesseract – Python wrapper for Tesseract
Matplotlib/Seaborn – Visualizations (optional)
PIL (Pillow) – Image processing

🔍 Key Features

📸 Image Preprocessing: Includes resizing, grayscale conversion, thresholding, and noise removal to enhance OCR accuracy.
🧠 Text Extraction: Uses Tesseract OCR to extract raw text from the cheque image.
🧾 Field Segmentation: Attempts to isolate key fields like:
      Payee Name
      Amount (in words and digits)
      Account Number
      IFSC Code
      Date

📦 Postprocessing: Basic pattern matching (e.g., regex) to extract structured information from raw OCR results.

▶️ How to Run

Install dependencies:
  pip install opencv-python pytesseract Pillow matplotlib

Install Tesseract OCR engine:
  Windows: Tesseract Installer
  Linux/macOS: Use your package manager (apt, brew, etc.)

Add Tesseract path to your environment (Windows only):
  pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'

Run the notebook:
  jupyter notebook "Bank Cheque OCR.ipynb"
  
📌 Notes

OCR accuracy depends on the quality of cheque images. High resolution and good contrast improve results.
Handwritten cheques may require fine-tuned OCR or deep learning-based handwriting recognition.
This is a prototype. For production use, consider layout-aware OCR tools like Google Vision API, Microsoft Read API, or LayoutLM.
