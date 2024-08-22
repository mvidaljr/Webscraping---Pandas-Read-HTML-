# Webscraping with Pandas and urllib

## Project Overview

This project demonstrates the use of the `urllib.request` and `Pandas` libraries for web scraping. The focus is on navigating HTML code and extracting tables directly from web pages using Pandas.

## Tools & Libraries Used

- **Data Collection:**
  - `urllib.request` for making HTTP requests to fetch HTML content.
- **Data Extraction:**
  - `Pandas` for parsing and extracting tables from the HTML content.

## Methodology

### Data Collection:

- Utilized `urllib.request` to retrieve HTML content from a specified URL.
- Loaded the HTML content into Pandas for further processing.

### Data Extraction:

- Used `Pandas`' `read_html` function to locate and extract tables from the HTML content.
- Cleaned and structured the extracted data for analysis or storage.

## Example Usage

```python
import urllib.request
import pandas as pd

# Fetching HTML content
url = "http://example.com/table-page"
response = urllib.request.urlopen(url)
html_content = response.read()

# Extracting tables from HTML
tables = pd.read_html(html_content)
for table in tables:
    print(table)
```

## Results

The project successfully extracted HTML tables from a web page and processed them using Pandas, showcasing a simple yet powerful approach to web scraping.

## Conclusion

This project highlights the effectiveness of combining `urllib.request` and `Pandas` for web scraping tasks, particularly when working with tabular data on web pages.

## Future Work

- Expand the project to handle more complex HTML structures or dynamic content using additional tools like `BeautifulSoup` or `Selenium`.
- Automate data extraction from multiple pages or websites for larger datasets.

