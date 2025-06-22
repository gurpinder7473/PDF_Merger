# PDF_Merger

# PDF-Merger

This Python script allows you to merge multiple PDF files into a single PDF file. The script uses the `PyPDF2` library to handle PDF manipulation.

## Requirements

- Python 3.x
- `PyPDF2` library

You can install the required library using pip:

```bash
pip install PyPDF2
```

## Usage

1. **Clone the Repository**

2. **Set the paths**

   Modify the script to include the paths of the PDFs you want to merge and the output file name. Example:

   ```python
   input_pdfs = ["/path/to/part1.pdf", "/path/to/part2.pdf"]
   output_pdf = "merged_output.pdf"
   merge_pdfs(input_pdfs, output_pdf)
   ```

3. **Run the Script**

   ```bash
   python merge_pdfs.py
   ```

4. **Merged PDF**

   The merged PDF will be saved with the name specified in the `output_pdf` variable.

## Script Explanation

### merge_pdfs Function

This function takes two arguments:
- `input_pdfs`: A list of paths to the input PDF files to be merged.
- `output_pdf`: The path where the merged PDF file will be saved.

The function performs the following steps:
1. Creates a `PdfWriter` object.
2. Iterates over each input PDF file:
   - Opens the PDF file.
   - Reads the PDF file using `PdfReader`.
   - Adds each page of the PDF to the `PdfWriter` object.
   - Closes the PDF file.
3. Writes the combined pages to the output PDF file.


## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
