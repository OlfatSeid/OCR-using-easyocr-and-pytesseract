# OCR PDF Extraction and Annotation

This repository contains Python notebooks that perform Optical Character Recognition (OCR) on PDF documents. The notebooks extract text along with confidence scores, annotate the detected text in the images, and save the results in various formats. There are two versions available: one using EasyOCR and another using PyTesseract.

## Features

- **Multi-language OCR Support**: The EasyOCR notebook supports OCR in both English and Arabic, while the PyTesseract notebook is configured for English.
- **Bounding Box Creation**: Draws bounding boxes around detected text in the PDF pages.
- **Confidence Scores**: Extracts and displays confidence scores for each detected text instance.
- **Save Results**:
  - Extracted text is saved as plain text files.
  - Bounding boxes and extracted text data are saved in JSON format.
  - Annotated PDF pages are saved as a single PDF file.
  - Each detected text region is saved as an individual image.


### Prerequisites

Before running the notebooks, ensure you have the following installed:

- Python 3.x
- Jupyter Notebook
- Required Python libraries (listed below)

### Install Required Libraries

You can install the required libraries using pip:

```bash
pip install easyocr pytesseract pdf2image opencv-python-headless matplotlib Pillow tqdm

## Output
Text Files: Contains the extracted text for each page.
JSON Files: Contains bounding box coordinates, confidence scores, and paths to extracted text images.
Annotated PDF: A PDF with the original pages and annotated bounding boxes around the detected text.