# PDF Document Processing and TF-IDF

A Natural Language Processing project that extracts text from multiple PDF documents and represents them using manually implemented Term Frequency (TF), Inverse Document Frequency (IDF), and TF-IDF.

## Pipeline
1. Read PDF files and extract page text using PyPDF2.
2. Lowercase and clean the extracted text.
3. Tokenize with NLTK.
4. Remove English stopwords.
5. Calculate TF for each document.
6. Calculate IDF across the document collection.
7. Calculate TF-IDF and build a document-term matrix.
8. Display top-ranked terms and export results.

## Dataset / input documents
This project uses user-provided PDF documents. Create a folder named `pdf_documents` beside the notebook and place one or more text-based `.pdf` files inside it.

The original assignment used PDFs stored in `/content/Task2`; this version uses the portable local folder `pdf_documents/` instead. The actual source PDFs are not included in this ZIP because they were not supplied with the notebook.

**Important:** Scanned/image-only PDFs may not contain an extractable text layer. OCR is not included in this project.

## Project structure
```text
PDF-Document-Processing-TF-IDF/
├── PDF_Document_Processing_TF_IDF.ipynb
├── README.md
├── requirements.txt
└── pdf_documents/
    └── your_pdf_files.pdf
```

## Run locally
```bash
python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate

pip install -r requirements.txt
jupyter notebook
```
Open `PDF_Document_Processing_TF_IDF.ipynb` and run all cells.

## Generated outputs
The notebook creates an `outputs/` folder containing:
- `tfidf_document_term_matrix.csv`
- `top_tfidf_terms.csv`
- `document_summary.csv`

Run the notebook with your own PDF files before publishing these outputs. They are not included as fabricated sample results.

## TF-IDF formula
`TF-IDF(term, document) = TF(term, document) × log(N / DF(term))`

where `N` is the number of documents and `DF(term)` is the number of documents containing the term.

## Technologies
Python, PyPDF2, NLTK, NumPy, Pandas, Matplotlib, Jupyter.
