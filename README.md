# PDF_Merger

# 📎 PDF Merger

A simple Python script to merge multiple PDF files into a single PDF document using the [`PyPDF2`](https://pypi.org/project/PyPDF2/) library.

---

## ✅ Features

- Merge multiple PDFs into one
- Lightweight and easy to use
- Customizable input and output paths

---

## 🧰 Requirements

- Python 3.x
- PyPDF2 library

Install the required library using:

```bash
pip install PyPDF2
```

---

## 🚀 How to Use

### 1. Clone or Download

Download or clone this repository to your local machine.

### 2. Set PDF Paths

Edit the script to include your input PDF file paths and desired output file name:

```python
input_pdfs = ["file1.pdf", "file2.pdf", "file3.pdf"]
output_pdf = "merged_result.pdf"
merge_pdfs(input_pdfs, output_pdf)
```

### 3. Run the Script

Run the script from your terminal:

```bash
python merge_pdfs.py
```

### 4. Result

The merged PDF will be saved with the name specified in `output_pdf`.

---

## 🧠 Script Overview

### `merge_pdfs` Function

```python
def merge_pdfs(input_pdfs, output_pdf):
    writer = PdfWriter()
    for file in input_pdfs:
        reader = PdfReader(file)
        for page in reader.pages:
            writer.add_page(page)
    with open(output_pdf, "wb") as f:
        writer.write(f)
```

- **`input_pdfs`**: List of PDF files to be merged.
- **`output_pdf`**: Output file name for the merged PDF.

---

## 📄 Example

```python
from PyPDF2 import PdfReader, PdfWriter

def merge_pdfs(input_pdfs, output_pdf):
    writer = PdfWriter()
    for pdf in input_pdfs:
        reader = PdfReader(pdf)
        for page in reader.pages:
            writer.add_page(page)
    with open(output_pdf, "wb") as output_file:
        writer.write(output_file)

# Example usage
input_pdfs = ["part1.pdf", "part2.pdf"]
output_pdf = "merged_output.pdf"
merge_pdfs(input_pdfs, output_pdf)
```

---

## 📝 License

This project is licensed under the MIT License.


