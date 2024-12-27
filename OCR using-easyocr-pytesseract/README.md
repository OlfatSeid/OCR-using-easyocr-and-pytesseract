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


### Prerequisites

- Before running the notebooks, ensure you have the following installed:

- Python 3.x
- Jupyter Notebook
- Required Python libraries (listed below)
-----------------------------
### Install Required Libraries

You can install the required libraries using pip:

                   pip install easyocr pytesseract pdf2image opencv-python-headless matplotlib Pillow tqdm

## Output
Text Files: Contains the extracted text for each page.
JSON Files: Contains bounding box coordinates, confidence scores, and paths to extracted text images.
Annotated PDF: A PDF with the original pages and annotated bounding boxes around the detected text.



### Usage

Step 1: Initialize the OCR Readers
The script initializes EasyOCR readers for Arabic and English text.

                            arabic_reader = easyocr.Reader(['ar'], gpu=True)
                            english_reader = easyocr.Reader(['en'], gpu=True)
