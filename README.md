# PDF-to-Text
Python CLI tool that recursively converts PDF files in a directory into plain text files

# PDF to Text Converter (Recursive, Cross-Platform)

A production-ready Python CLI tool that recursively converts PDF files in a directory into plain text files.

 Cross-platform (Windows, Linux, macOS)  
 No system-level dependencies (pip-only)  
 Recursive directory processing  
 Preserves folder structure  
 Automatic fallback between extraction engines  
 Logging included  

---

## Features

- Fast extraction using **PyMuPDF**
- Automatic fallback to **pypdf** if text extraction is weak
- Recursively scans directories for `.pdf` files
- Preserves the original directory structure
- Handles large PDF files
- Clean CLI interface
- Error logging to file

---

## Installation

Clone the repository:

```bash
git clone https://github.com/frankcasas/PDF-to-Text.git
cd PDF-to-Text
```
Install dependencies:
```bash
pip install -r requirements.txt
```
Or install manually:
```bash
pip install pymupdf pypdf tqdm
```
 Usage
The script requires:

--input → Directory containing PDF files

--output → Directory where text files will be saved

Example
```bash
python pdf_to_text.py --input ./pdfs --output ./text_output
```

Windows Example
```bash
python pdf_to_text.py --input "C:\Users\me\Documents\pdfs" --output "C:\Users\me\Documents\output"
```
 How It Works
The script recursively scans the input directory for .pdf files.

Extracted text is saved as .txt files.

The original directory structure is preserved inside the output folder.

Example
Input structure:
```markdown
pdfs/
├── file1.pdf
└── reports/
    └── report1.pdf
```
Output structure:
```markdown
text_output/
├── file1.txt
└── reports/
    └── report1.txt
```
 Logging
 
All errors and fallback events are written to:
```lua
pdf_processing.log
```
This file is automatically created in the project root.

 Limitations
Image-only (scanned) PDFs are not supported in this version.

OCR requires an external engine (e.g., Tesseract) and is intentionally not included to keep the project dependency-free.

Requirements
```nginx
pymupdf
pypdf
tqdm
```
