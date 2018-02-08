## Welcome to webscrape

This website is dedicated to teach people how to scrape web properly and efficiently. The language we will be using here will be [Python](https://www.python.org/).

### Web Scraping

Web Scraping is the process of extracting data from the web automatically using some tools or code.
Python is one of the most popular language used for web scraping. Python is easy to learn and deploy.


Below is a simple [Scrapy](https://scrapy.org/) script, a Python framework used for web scraping.

```markdown
import scrapy

class ExampleSpider(scrapy.Spider):
    name = 'example'
    allowed_domains = ['example.com']
    start_urls = ['http://www.example.com/']

    def parse(self, response):
        heading = response.css('h1::text').extract_first()
        text = response.css('p::text').extract_first()
        yield {
            'heading': heading,
            'text': text,
        }
```

### Popular Python Frameworks/Libraries for web scraping

* [urllib](https://docs.python.org/3/library/urllib.html): Python's native package for playing with url.

* [requests](http://docs.python-requests.org/en/master/): A simple python library that allow us to send HTTP requests.

* [lxml](http://lxml.de/): A fantastic and fast library for parsing XML and HTML documents.

* [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/): Another great library for parsing XML and HTML documents. 
While lxml is fast, BeautifulSoup is easy to use.

* [Selenium](http://www.seleniumhq.org/): An automation tool for testing web applications which can also be used for web scraping. 
Selenium is available in other languages like Java, C#, Ruby, etc.

* [Scrapy](https://scrapy.org/): A robust framwework for scraping data in a manageable and efficient way. 
Ultimately, scrapy is the one to choose in order to scrape web data in a scalable way. 