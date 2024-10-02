# E-Com_webScrap

**This script scrapes product data (name, price, and availability) from an e-commerce website and stores it in a SQLite database. The data can then be exported to a CSV file for further analysis.

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
#### *Note: E-com websites like Amazon, Flipkart are secured and does not allow to webscrap. As we use a simple website to test the programme.*

## Sample Output
``` 
Enter the URL :  https://books.toscrape.com/catalogue/category/books/science_22/index.html 
Data has been saved to product_data.csv
```
##### [product_data.csv](https://github.com/user-attachments/files/17184763/product_data.csv)

#### Open the .ipynb in Jupyter Notebook or Copy the code to any editor and run the code. It will ask to enter the URL and data will be saved to product_data.csv file.
