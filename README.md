# Walmart Product Scraper

This Python script scrapes product information from Walmart's website using a list of search queries. It extracts details such as price, review count, rating, and product descriptions, saving the data in a JSONL file.

## Features

- Scrapes product information from Walmart's search results
- Uses proxy rotation to avoid IP blocks
- Implements error handling and retries for robust scraping
- Saves product data in JSONL format

## Requirements

- Python 3.6+
- Required Python packages:
  - requests
  - beautifulsoup4
  - python-dotenv

## Setup

1. Clone this repository or download the script.
2. Install the required packages:
```bash
pip install requests beautifulsoup4 python-dotenv
```
3. Create a `.env` file in the same directory as the script with your Bright Data credentials:
```bash
BRD_USERNAME=your_username
BRD_PASSWORD=your_password
```
## Usage

Run the script with:

python walmart_scraper.py

The script will start scraping product information based on the predefined search queries. The results will be saved in `product_info.jsonl` in the same directory.

## Configuration

- Modify the `search_queries` list to change or add search terms.
- Adjust the `BASE_HEADERS` dictionary if you need to update the user agent or other headers.
- The script is set to scrape up to 99 pages per search query. You can modify this limit in the `main()` function.

## Output

The script generates a JSONL file named `product_info.jsonl`. Each line in this file is a JSON object containing information about a single product, including:

- Price
- Review count
- Item ID
- Average rating
- Product name
- Brand
- Availability
- Image URL
- Short description

## Note

This script uses proxy servers from Bright Data. Ensure you have an active subscription and correct credentials in your `.env` file.

## Disclaimer

Web scraping may be against the terms of service of some websites. Use this script responsibly and ensure you have permission to scrape the target website.

# Advanced Web Scraping Tutorial From the Creator
<img src="./images/thumbnail.jpg" width="50%"/>
<br/>

Code corresponding to my [recent video](https://youtu.be/DcI_AZqfZVc) on web scraping with Python BeautifulSoup

## About/Navigation
At certain parts of the video, I reference accessing the code at different stages of completeness. 

Here are the files that you may be looking for:
- [Initial Run - 24:50 in video](https://github.com/KeithGalli/advanced-scraping/commit/5afbdd59e4982c1a6ce7ad1fe9cb5047eaf8ac25)
- [Improvements - 27:19 in video](https://github.com/KeithGalli/advanced-scraping/blob/original/search_scraper.py)
- [Final Code w/ Proxies](./search_scraper.py)

Make sure to add a **.env** file when you start using the Bright Data proxies!

Shout out to Bright Data for sponsoring this video, get started using [this link](https://brdta.com/keithgalli)!
