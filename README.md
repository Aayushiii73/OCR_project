# OCR_project
Optical Character Recognition (OCR) Project

Overview

This project involves building an Optical Character Recognition (OCR) system capable of detecting both mathematical expressions and alphabetical text. The primary goal is to process input PDFs, extract text (including LaTeX for mathematical expressions), and evaluate answer sheets by comparing the extracted text with correct answer keys.

Key Features

Dual OCR System: LatexOCR is used for detecting mathematical expressions and converting them into LaTeX code.
Pytesseract is employed for extracting alphabetical text.

Input Handling: The input is a PDF document. Images are generated for each page, and bounding boxes around paragraphs are identified for processing.

Text Processing: Outputs from LatexOCR and Pytesseract are combined. A GPT-2 model is used for post-processing, ensuring the final LaTeX code for each bounding box is correct and coherent.

Answer Sheet Evaluation: Extracted text is compared with correct answer keys using cosine similarity. Scores are calculated for each answer sheet based on the similarity results.

Workflow

1. PDF to Images: Convert each page of the PDF into images.

2. Bounding Box Detection: Identify bounding boxes around paragraphs in the images.
   ![image](https://github.com/user-attachments/assets/97dca63e-71a1-431f-9c21-7c5b9d796ec8)


3. OCR Processing:
Feed each bounding box into the combined OCR system.
Generate LaTeX code for mathematical expressions and extract alphabetical text.

4. Post-Processing:
Use GPT-2 to refine and combine outputs into final LaTeX code for each bounding box.

5. Answer Sheet Scoring:
Compare extracted text with answer keys using cosine similarity. Generate scores for each answer sheet.

Dependencies

OCR Tools:
1. LatexOCR
2. Pytesseract

AI Model: GPT-2

Image Processing: Libraries for handling PDFs and images (e.g., PyPDF2, Pillow)

Similarity Calculation: Libraries for cosine similarity (e.g., scikit-learn)

Use Cases
1. Automated evaluation of answer sheets in educational settings.
2. Extraction and processing of both mathematical and textual data from documents.

Installation

Clone the repository: git clone https://github.com/Aayushiii73/OCR_project.git

Install the required dependencies: pip install -r requirements.txt

Usage: Place the input PDF in the input folder.

Run the main script: python main.py

The output will include: Extracted LaTeX code and Scoring results for each answer sheet.

Contributing
We welcome contributions! Please feel free to submit issues or pull requests to improve this project.

Acknowledgments
Thanks to the developers of LatexOCR, Pytesseract, and GPT-2 for providing powerful tools that made this project possible.
