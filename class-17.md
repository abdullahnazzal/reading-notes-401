
# Web Scraping

Web scraping is a technique to automatically access and extract large amounts of information from a website, which can save a huge amount of time and effort. In this article, we will go through an easy example of how to automate downloading hundreds of files from the New York MTA. 

This is a great exercise for web scraping beginners who are looking to understand how to web scrape. Web scraping can be slightly intimidating, so this tutorial will break down the process of how to go about the process.

## **There’s a big challenge in data science New York MTA Data**

We will be downloading turnstile data from this site:

http://web.mta.info/developers/turnstile.html

Turnstile data is compiled every week from May 2010 to present, so hundreds of .txt files exist on the site. Below is a snippet of what some of the data looks like. Each date is a link to the .txt file that you can download.

## **Important notes about web scraping:**

    1- Read through the website’s Terms and Conditions to understand how you can legally use the data. Most sites prohibit you from using the data for commercial purposes.

#

    2- Make sure you are not downloading data at too rapid a rate because this may break the website. You may potentially be blocked from the site as well.

## **Python Code**

We start by importing the following libraries.

```py
import requests
import urllib.request
import time
from bs4 import BeautifulSoup
```

Next, we set the url to the website and access the site with our requests library.

```py
url = 'http://web.mta.info/developers/turnstile.html'
response = requests.get(url)
```


Next we parse the html with BeautifulSoup so that we can work with a nicer, nested BeautifulSoup data structure. If you are interested in learning more about this library, check out the BeatifulSoup documentation.

```py
soup = BeautifulSoup(response.text, “html.parser”)
```
We use the method .findAll to locate all of our <a> tags.
```py
soup.findAll('a')
```
***

**To know more please [visit this page](https://towardsdatascience.com/how-to-web-scrape-with-python-in-4-minutes-bc49186a8460)**

***

