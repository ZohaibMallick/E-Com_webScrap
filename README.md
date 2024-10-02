# E-Com_webScrap

**This script scrapes product data (name, price, and availability) from an e-commerce website and stores it in a SQLite database. The data can then be exported to a CSV file for further analysis.**

## Prerequisites

- Python 3.x
- The following Python libraries:
  - `requests`
  - `beautifulsoup4`
  - `pandas`
  - `sqlite3`
- Install the required libraries using:
  ```bash
  pip install requests beautifulsoup4 pandas


### ***Sample URL:***
##### '''https://books.toscrape.com/catalogue/category/books/science_22/index.html'''
#### *Note: 
  - E-com websites like Amazon, Flipkart are secured and does not allow to webscrap. As we use a simple website to test the programme.
  - Make sure to adhere to the website's terms of service and scraping policies.
  - Modify the CSS selectors (.product, .product-name, .product-price, .product-availability) as needed to match the target website's HTML structure.

## Sample Output
``` 
Enter the URL :  https://books.toscrape.com/catalogue/category/books/science_22/index.html 
Data has been saved to product_data.csv
```
##### [product_data.csv](https://github.com/user-attachments/files/17184763/product_data.csv)

#### Open the .ipynb in Jupyter Notebook or Copy the code to any editor and run the code. It will ask to enter the URL and data will be saved to product_data.csv file.


![webscrap](https://github.com/user-attachments/assets/9f494fc8-ecd0-4eea-9310-52006fec96e9)

### Workflow Description:
  - Scraping Products: The script starts by initializing a SQLite database and creates a 'products' table if it does not exist. It then enters a loop, building URLs with a page number and using requests to fetch each page. The pages are parsed using BeautifulSoup to extract product details.

  - Data Storage: The extracted product information (name, price, availability) is inserted into the SQLite database. The diagram shows the insertion step, indicating that data is stored as it is scraped from each page.

  - Pagination: The script continues to loop through pages, checking if there are more products to scrape. It stops when it encounters an error (e.g., a 404 response) or when there are no more products. This process is controlled by the "Response OK?" decision node.

  - Exporting to CSV & Respectful Scraping: After completing the scraping, the data is exported to a CSV file. The diagram also includes a delay between requests to avoid overloading the server, demonstrating a "respectful scraping" practice.
