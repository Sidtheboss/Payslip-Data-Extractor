# Payslip Data Extractor

## -> Overview
This project extracts key details from a payslip image (JPG/PNG) using Optical Character Recognition (OCR) and Natural Language Processing (NLP). The extracted information includes:
- Employee Name
- Designation
- Total Earnings
- Net Pay

##  Features
- **Uses Tesseract OCR (`pytesseract`)** to extract text from images.
- **Preprocessing techniques** (grayscale conversion, noise removal, thresholding) to enhance text clarity.
- **Regex-based entity extraction** for structured data.
- **Colab-friendly script** for easy execution.

## 🛠️ Installation
Before running the script, install the required dependencies:
```sh
pip install pytesseract opencv-python numpy google-colab
apt-get install -y tesseract-ocr
```

## How to Use
1. Upload a payslip image (`.jpg`/`.png`) in Google Colab.
2. Run the script to extract payslip details.
3. View structured output.

##  Running the Code
```python
from google.colab import files
uploaded = files.upload()
file_path = list(uploaded.keys())[0]

extracted_data = process_payslip(file_path)
print(extracted_data)
```

## Key Functions
- `preprocess_image(image_path)`: Enhances image for better OCR.
- `extract_text_from_image(image_path)`: Extracts raw text using `pytesseract`.
- `extract_entities(text)`: Uses regex to extract required fields.
- `process_payslip(file_path)`: Main function to process payslip images.

##  Improvements
- Fine-tuned regex to extract `Total Earnings` and `Net Pay` more accurately.
- Applied advanced image preprocessing for better OCR performance.
- Future scope: Using deep learning-based entity recognition (e.g., LayoutLM).

## Author
Developed by **Siddharth**



