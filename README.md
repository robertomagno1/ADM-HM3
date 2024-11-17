# ADM-HM3

# Algorithmic Methods for Data Mining - Homework 3

 This is a Github repository created to submit the third Homework of the **Algorithmic Methods for Data Mining (ADM)** course for the MSc. in Data Science at the Sapienza University of Rome.


## What's inside this repository?

1. `README.md`: A markdown file that explains the content of the repository.

2. `main.ipynb`: A [Jupyter Notebook](https://nbviewer.org/github/msancor/ADM-HW3/blob/main/main.ipynb) file containing all the relevant exercises and reports belonging to the homework questions, the *Command Line Question*, and the *Algorithmic Question*.

 32 | ## Datasets
 33 | 
 34 | The data used to work in this repository was obtained by performing web-scraping in the [MSc. Degrees](https://www.findamasters.com/masters-degrees/msc-degrees/) website via the `WebScraper` class contained in the `web_scraper.py` module. If you want to reproduce the data perform the following steps:
 35 | 
 36 | **1.** Create the directories where you will save the obtained `html` and `tsv` files after you perform web-scraping. Specifically, run in your terminal the following commands:
 37 | 
 38 | ```bash
 39 | mkdir data
 40 | mkdir data/htmls
 41 | mkdir data/tsvs
 42 | ```
 43 | 
 44 | Make sure you create these folders in the same directory you've saved the `main.ipynb` file on.
 45 | 
 46 | **2.** Open the `main.ipynb` file and run the cells contained in the **Data Collection** section and you will obtain all the pertinent data files.
 47 | 
 48 | Alternatively, you can also just create a new `.py` file and run the following script:
 49 | 
 50 | ```python
 51 | from modules.web_scraper import WebScraper
 52 | from modules.html_parser import HTMLParser
 53 | 
 54 | #First, we have to initialize the WebScraper and HTMLParser classes by calling their constructors
 55 | web_scraper = WebScraper()
 56 | html_parser = HTMLParser()
 57 | 
 58 | #Here, the method saves scraped URLs from the website in a text file called urls.txt
 59 | web_scraper.scrape_urls()
 60 | 
 61 | #Here, we can call the .scrape_htmls() method to get the HTMLs of the URLs mentioned above.
 62 | web_scraper.scrape_htmls()
 63 | 
 64 | #Finally, you can parse the obtained HTMLs to obtain information about the courses and save it in .tsv files.
 65 | html_parser.parse_htmls()
 66 | 
 67 | #If you want to visualize the information obtained, you can store it in a dataframe
 68 | df = html_parser.get_dataframe()
 69 | df.head()
 70 | ```
 71 | 
 72 | Take into account this script will take $\sim 11$ hours so run it only if necessary.
 73 | 
 74 | ## API Usage
 75 | 
 76 | In order to plot a map with our results using the `MapPlotter` class defined before we used two external API's:
 77 | 
 78 | - [Google Maps API](https://mapsplatform.google.com/pricing/)
 79 | 
 80 | - [Mapbox API](https://docs.mapbox.com/api/overview/)
 81 | 
 82 | In order to gain access to these API's we had to create accounts and obtain **API keys** from each API. These keys were stored in a `.env` file and then read directly into the `map_plotter.py` module. Because of privacy issues this file is not included in our repository but can be recreated by any user with their own API keys. To do this follow these steps:
 83 | 
 84 | 1. Obtain API keys for both the [Google Maps API](https://mapsplatform.google.com/pricing/) and [Mapbox API](https://docs.mapbox.com/api/overview/).
 85 | 
 86 | 2. Create a `.env` file including the following:
 87 | 
 88 |     ```shell
 89 |     GOOGLE_API_KEY =
 90 |     MAPBOX_API_KEY =
 91 |     ```
 92 | 
 93 |     and write your API keys in the other side of the equal sign.
 94 | 
