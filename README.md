# File Comparison Tool

A browser-based tool for comparing two CSV, XLSX, or QVD files row by row. No server, no installation — go to https://bitmetric-bv.github.io/local-file-compare and everything runs locally in the browser.

<img width="2372" height="1258" alt="Schermopname_23-4-2026_134223_bitmetric-bv github io" src="https://github.com/user-attachments/assets/87b533b2-8ef8-4631-a931-e5427940d1b9" />

## Features

- Supports CSV, XLSX/XLS, and QVD (QlikSense / QlikView) files
- Select a key column to join rows across both files
- Select one or more value columns to compare
- Detects numeric differences and displays them with sign and two decimal places
- Identifies rows present in only one file
- Filter results by status: matches, differences, only in A, only in B
- Search by key value
- Click any key cell to copy it to the clipboard
- Export results to CSV
- Virtual scrolling handles large datasets without performance issues
- All processing runs in a Web Worker to keep the UI responsive

## Usage

1. Go to https://bitmetric-bv.github.io/local-file-compare in your browser.
2. Upload File A and File B using the sidebar.
3. Select a key column (used to match rows between the two files).
4. Select the value columns to compare.
5. Click **Compare files**.

## Privacy

No data leaves the browser. Files are parsed and compared entirely on the client side.

## Dependencies

Vendored in `vendor/`, no CDN or internet connection required.

- [PapaParse 5.4.1](https://www.papaparse.com/) — CSV parsing
- [SheetJS 0.18.5 (xlsx)](https://sheetjs.com/) — XLSX/XLS parsing
- QVD parsing is implemented natively — no external library needed
