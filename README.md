# Inaportnet Vessel Report Scraper

Python scraper that automates downloading LK3 LN vessel report data from the public Inaportnet monitoring website of the Indonesian Ministry of Transportation, covering all ports per month, then merges the files into one Excel dataset.

## How it works
1. Playwright (headless Chromium) opens the monitoring page for a given month and year.
2. The script collects every port's "LK3 LN" download link across all table pages.
3. Each report file is downloaded, parsed (HTML table or Excel), and tagged with port name and port code.
4. All ports are merged into one `.xlsx` file, and the raw files are zipped.

## Usage (Google Colab)
1. Open `inaportnet_scraper.ipynb` in Google Colab.
2. Set `BULAN_LIST` (months), `TAHUN` (year), and `DELAY` (seconds between requests).
3. Run all cells in order. Results download as `hasil_lk3_ln.zip`.

## Tech stack
Python, Playwright, pandas, openpyxl, BeautifulSoup, lxml, tqdm
