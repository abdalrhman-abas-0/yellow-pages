# YELLOW PAGES LEAD GENERATION

* this scraper is used to get the following information for lead generation and save it in a .csv file.
* this scraper is compiled in a way that avoids connection interruptions.
* it scrapes the leads information on two stages:

## **primary stage**
> Business Name

> Profile

> Phone Number

> Address

> Website

> Rating

> Review Count


## **secondary stage**
> Catagories

> Neighborhoods

> Extra Phones

> e-mail

> Other Links

> Social Media


> all the info scraped will be joined in one csv file at the end of the scraping process.

## Inputs:
  * search_subject: the leads to search for.
  * search_location: the location of the search.
  * pages_to_scrape: the number of pages to scrape.
  * site_name: always "Yellow Pages".
  * record_file: the text file that records the scraping process in case of an uncompleted previous scrape, enter "no" if a new scrape project is wished to be initiated.
  * url: the starting page url (must search for the subject and location on a browser first and then take the url and plug it in the scraper to start the program).

## Files Used:
* the .txt tracker file and the .csv files are created in the "outputs" folder.

1. controls.json:
* this file stores the following values which can be changed while the scraper is running:
  a. requests headers
  b. Breaker:if set to true it terminates the scraping process.
  c. nab:time in seconds which the scraper uses to sleep between the requests in case of a request interruption.

2. tracker file:
a .txt file records the progress of the scraping process and can be used to build up on uncompleted scraping from a previous time.

3. .csv files:
  a. primary files: individually scraped for each primary stage iteration.
  b. PRIMARY file: the concatenated final result of the primary stage.
  a. secondary files: individually scraped for each secondary stage iteration.
  b. SECONDARY file: the concatenated final result of the secondary stage.
  c. the final output file will be named in the following format ({site_name} {search_subject} in {search_location}.csv)

> when the scraping process is successfully completed all the primary/PRIMARY, secondary/SECONDARY & the txt tracker files will be deleted automatically.
