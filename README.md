# py-ground

A repository of utilities that I've written for personal use.

It so far includes a script for extracting pages from a PDF file with optional text highlighting.

## Utilities

### pdf-cherry-pick
#### Features

- Extract specific pages from a PDF file
- Highlight specified text in the extracted pages

#### Requirements

- Python 3.9 or higher
- `pymupdf` library

#### Installation

To install the required dependencies, run:

```sh
uv init
uv sync
```

#### Usage
To use the pdf-cherry-pick script, run the following command:
```sh
./pdf-cherry-pick <file_path> <page_numbers> [options]
```

##### Arguments
- `<file_path>`: Path to the PDF file
- `<page_numbers>`: Page numbers to extract
##### Options
- `-H, --highlight-text`: Text to highlight in the extracted pages. Repeat this option to highlight multiple texts.
- `-o, --output`: Output file path. Default is output.pdf.
- `-s, --output-suffix`: Suffix to append to the output file name. The file will be created in the current directory with the suffix appended to the original file name.

**Example**:
```sh
./pdf-cherry-pick example.pdf 1 2 3 -H "important" -o output.pdf
```

This command extracts pages 1, 2, and 3 from `example.pdf`, highlights the word "important" in the extracted pages, and saves the result to output.pdf.

---
