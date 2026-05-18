# Extracting and Visualizing Stock Data

A Python data science project that extracts historical stock prices and quarterly revenue data for **Tesla (TSLA)** and **GameStop (GME)**, then visualizes them side-by-side in a two-panel dashboard.

---

## Overview

This notebook demonstrates two common data-gathering techniques in data science:

- **API-based extraction** — pulling historical stock price data via the `yfinance` library
- **Web scraping** — extracting quarterly revenue tables from HTML pages using `requests` and `BeautifulSoup`

The extracted data is then cleaned and plotted using `matplotlib` to produce a dashboard showing share price and revenue trends up to June 2021.

---

## Project Structure

```
Revenue_Data_and_Building_a_Dashboard.ipynb   # Main notebook
README.md
```

---

## Questions / Sections

| # | Task |
|---|------|
| 1 | Extract Tesla stock data using `yfinance` |
| 2 | Scrape Tesla quarterly revenue data |
| 3 | Extract GameStop stock data using `yfinance` |
| 4 | Scrape GameStop quarterly revenue data |
| 5 | Plot Tesla stock price & revenue dashboard |
| 6 | Plot GameStop stock price & revenue dashboard |

---

## Requirements

Install dependencies before running the notebook:

```bash
pip install yfinance bs4 nbformat matplotlib pandas
```

| Library | Purpose |
|---------|---------|
| `yfinance` | Download historical stock data from Yahoo Finance |
| `requests` | Fetch HTML pages for web scraping |
| `beautifulsoup4` | Parse HTML and extract revenue tables |
| `pandas` | Data manipulation and cleaning |
| `matplotlib` | Static chart generation |

---

## Usage

1. Clone the repository and open the notebook:
   ```bash
   git clone <your-repo-url>
   cd <repo-folder>
   jupyter notebook Revenue_Data_and_Building_a_Dashboard.ipynb
   ```

2. Run all cells in order. The final two cells will render dashboards like this:

   - **Top panel** — Historical share price (up to June 2021)
   - **Bottom panel** — Quarterly revenue in USD millions (up to April 2021)

---

## Key Functions

### `make_graph(stock_data, revenue_data, stock)`

Renders a two-panel matplotlib figure for a given stock.

| Parameter | Type | Description |
|-----------|------|-------------|
| `stock_data` | `DataFrame` | Must contain `Date` and `Close` columns |
| `revenue_data` | `DataFrame` | Must contain `Date` and `Revenue` columns |
| `stock` | `str` | Stock name used as the chart title |

---

## Data Sources

- **Stock prices** — Yahoo Finance via `yfinance` (`period="max"`)
- **Tesla revenue** — IBM Skills Network hosted HTML table
- **GameStop revenue** — IBM Skills Network hosted HTML table

---

## Authors

- [Joseph Santarcangelo](https://www.linkedin.com/in/joseph-s-50398b136/) — IBM
- Azim Hirjani
- Malika Singla
- Lakshmi Holla

---

## License

© 2020 IBM Corporation. All rights reserved.
