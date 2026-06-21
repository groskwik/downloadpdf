# downloadpdf

Small Python script that searches Google for a PDF manual based on an eBay listing title, then downloads the first valid PDF it can find.

## Requirements

- Python 3.9+
- Google Chrome installed
- Python packages:
  - `requests`
  - `beautifulsoup4`
  - `selenium`

Install the Python packages with:

```powershell
python -m pip install requests beautifulsoup4 selenium
```

## Usage

Run the script from this directory:

```powershell
python downloadpdf.py
```

When prompted, paste an eBay listing title. The script cleans the title, searches Google for a matching PDF, and downloads the file if a valid PDF is found.

Downloaded files are saved in:

```text
downloaded_manuals/
```

## Generated Files

The script creates these folders automatically:

- `downloaded_manuals/` for downloaded PDFs
- `chrome_selenium_profile/` for the local Selenium Chrome profile

These folders do not need to exist before running the script.

## Notes

- Chrome may open while the script is running.
- Some websites block direct downloads, so the script first tries `requests` and then falls back to Selenium/Chrome.
- Google search results and PDF availability can vary, so the script may not find a PDF every time.
