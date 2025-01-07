# OCR PDF Extraction and Annotation

This repository contains Python notebooks that perform Optical Character Recognition (OCR) on PDF documents. The notebooks extract text along with confidence scores, annotate the detected text in the images, and save the results in various formats. There are two versions available: one using EasyOCR and another using PyTesseract.

## Features

1. ### Multi-Language OCR

- Supports Arabic and English languages using EasyOCR.

2. ### Box Creation

- Extracts text along with bounding box coordinates.

- Annotates the original images with bounding boxes around detected text.
3. ### JSON and Image Output

- Saves extracted text and bounding box data into individual JSON files.

- Cropped images of detected regions (ROIs) are saved separately.

4. ### Annotated PDF Generation

- Combines annotated images into a single PDF file for easy review.

5. ### Text File Output

- Outputs extracted text from all pages into a text file.

## Install required Python libraries:
You can install the required libraries using pip:

                   pip install easyocr pytesseract pdf2image opencv-python-headless matplotlib Pillow tqdm



### Usage

1: **Initialize the OCR Readers** 

The notebook initializes EasyOCR readers for Arabic and English text.
```python
                            arabic_reader = easyocr.Reader(['ar'], gpu=True)
                            english_reader = easyocr.Reader(['en'], gpu=True)
```
2: **Run OCR on PDFs** 

Call the ocr_pdf_to``_individual_json function for each PDF file.

Example for English PDF:
```python
                           english_pdf_path = '/path/to/english.pdf'
                           ocr_pdf_to_individual_json(english_pdf_path, language='en', output_dir="output_pdf_english", save_pdf=True)
```                        
Example for Arabic PDF: 
```python
                           arabic_pdf_path = '/path/to/arabic.pdf'
                           ocr_pdf_to_individual_json(arabic_pdf_path, language='ar', output_dir="output_pdf_arabic", save_pdf=True)
```
## Notes

- Ensure GPU support for faster OCR processing, especially for large PDFs.

- Modify the font path in the script (/content/DejaVuSansCondensed-Bold.ttf) as per your system's font availability.
