**Financial Report Table Extraction**

Project Overview :

This project focuses on extracting structured financial tables (Balance Sheet, Income Statement, and Cash Flow Statement) from PDF financial reports using Optical Character Recognition (OCR). Due to the unavailability of free multimodal LLM APIs (such as OpenAI GPT-4V, Google Gemini, Claude 3 Vision, and Grok), a Python-based OCR approach was implemented to process scanned financial documents. The extracted data is then standardized using a predefined vocabulary and formatted into Markdown and CSV for further analysis.

Tech Stack Used :

***Python** – Core programming language

***Tesseract OCR (pytesseract)** – Text extraction from scanned PDFs

***OpenCV** – Image preprocessing to improve OCR accuracy

***pdf2image** – Convert PDF pages into images for OCR processing

***pandas** – Data processing and table structuring

***tabulate** – Formatting extracted tables in Markdown format

***Regular Expressions (Regex)** – Cleaning and aligning extracted text

Project Workflow :

**Convert PDF to Images** – Extract individual pages using pdf2image.

**Preprocess Images** – Apply grayscale conversion and thresholding using OpenCV.

**Extract Text using OCR** – Use Tesseract OCR to recognize and extract financial table data.

**Structure and Standardize Data **– Process extracted text, clean misalignments, and apply vocabulary mapping for consistency.

**Output in Markdown & CSV** – Save structured financial tables in Markdown (.md) and CSV (.csv) formats.

(Question 3 Response) :

If given additional time, I would focus on the following improvements to enhance the accuracy, efficiency, and scalability of the extraction process:

**Enhancing OCR Accuracy & Preprocessing :**

Improve text recognition by optimizing image preprocessing techniques (denoising, adaptive thresholding, morphological transformations).

Experiment with different OCR modes (--psm 4, --psm 6) and evaluate alternative OCR engines like EasyOCR or Google Vision API for better structured extraction.

**Performance Optimization & Scalability :**

Parallelize OCR processing using Python’s multiprocessing to handle large reports efficiently.

Process images in batches instead of loading entire PDFs into memory to improve efficiency.

**Automated Data Standardization & Validation :**

Implement rule-based validation to ensure extracted tables follow financial reporting standards.

Cross-check extracted figures with publicly available financial reports for consistency.

**Extending Usability & Output Formats :**

Support multiple output formats (CSV, JSON, Excel) for integration with financial analysis tools.

Develop a web-based UI (Streamlit or Flask) where users can upload PDFs and receive structured outputs.

By implementing these enhancements, the system would become more accurate, scalable, and user-friendly, enabling seamless extraction and analysis of financial data from complex reports.
