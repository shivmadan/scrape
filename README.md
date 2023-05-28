# Text-scrape

This code is a basic web scraping script that fetches the content of a webpage and extracts the text within `<p>` tags. It utilizes the `requests` library to retrieve the webpage's HTML content and the `BeautifulSoup` library to parse and navigate the HTML structure.

## Setup
To use this code, make sure you have the following dependencies installed:
- `requests`
- `beautifulsoup4`

You can install these dependencies using `pip` by running the following command:
```
pip install requests beautifulsoup4
```

## Usage
1. Specify the URL of the webpage you want to scrape by assigning it to the `url` variable.
2. The code fetches the webpage's content using `requests.get()` and creates a `BeautifulSoup` object to parse the HTML.
3. It finds all `<p>` tags on the page using `soup.find_all('p')` and stores them in the `paragraphs` variable.
4. The text content of each `<p>` tag is printed to the console using `paragraph.text`.
5. The code also creates a file named `paragraph-1.txt` on the user's desktop to save the text content of each `<p>` tag.
6. The text content is then written to the file line by line.

Make sure to modify the `file_path` variable if you want to save the file to a different location.

Note: Ensure that you have the necessary permissions to write files to the specified directory.


## Limitations
- This code specifically targets `<p>` tags for extraction. Modify the code if you want to extract content from different HTML tags.
- The code assumes the webpage content is in valid HTML format. Unexpected HTML structure or errors in the page can cause issues.


# Text-Type Scrape

This is a variation of Text-scrape (above) that extracts the text from specific HTML tags based on the content type. 

It utilizes the `requests` library to retrieve the webpage's HTML content and the `BeautifulSoup` library to parse and navigate the HTML structure.

## Setup
To use this code, make sure you have the following dependencies installed:
- `requests`
- `beautifulsoup4`

You can install these dependencies using `pip` by running the following command:
```
pip install requests beautifulsoup4
```

## Usage
1. Specify the URL of the webpage you want to scrape by assigning it to the `url` variable.
2. The code fetches the webpage's content using `requests.get()` and creates a `BeautifulSoup` object to parse the HTML.
3. It finds the HTML type of the content by searching for a specific `<div>` element with the class name `'col-md-9'`.
4. If the `content_type` variable is not `None`, the code finds all tags within that content type using `content_type.find_all()`. Otherwise, an empty list is assigned to `content_tags`.
5. The text content of each tag in `content_tags` is printed to the console using `tag.text`.
6. The code also creates a file named `content.txt` on the user's desktop to save the text content of each tag.
7. The text content is then written to the file line by line.

Make sure to modify the `file_path` variable if you want to save the file to a different location.

Note: Ensure that you have the necessary permissions to write files to the specified directory.

## Limitations
- This code assumes that the specific HTML element with the class `'col-md-9'` represents the desired content type. Modify the code if you want to target different HTML elements or classes.
- The code may not work as expected if the webpage structure or class names change.
