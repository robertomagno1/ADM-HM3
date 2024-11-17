# ADM-HM3

# Algorithmic Methods for Data Mining - Homework 3

 This is a Github repository created to submit the third Homework of the **Algorithmic Methods for Data Mining (ADM)** course for the MSc. in Data Science at the Sapienza University of Rome.


## What's inside this repository?

1. `README.md`: A markdown file that explains the content of the repository.

2. `main.ipynb`: A [Jupyter Notebook](https://nbviewer.org/github/msancor/ADM-HW3/blob/main/main.ipynb) file containing all the relevant exercises and reports belonging to the homework questions, the *Command Line Question*, and the *Algorithmic Question*.

 ## Datasets

 The data used to work in this repository was obtained by performing web-scraping in the [MSc. Degrees](https://www.findamasters.com/masters-degrees/msc-degrees/) website via the `WebScraper` class contained in the `web_scraper.py` module. If you want to reproduce the data perform the following steps:

 **1.** Create the directories where you will save the obtained `html` and `tsv` files after you perform web-scraping. Specifically, run in your terminal the following commands:

 ```bash
 mkdir data
 mkdir data/htmls
 mkdir data/tsvs
```

 Make sure you create these folders in the same directory you've saved the `main.ipynb` file on.

 **2.** Open the `main.ipynb` file and run the cells contained in the **Data Collection** section and you will obtain all the pertinent data files.
