# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Web Scraping with Beautiful Soup

In this project, you will use `BeautifulSoup` to scrape [https://pages.git.generalassemb.ly/rldaggie/for-scraping/](https://pages.git.generalassemb.ly/rldaggie/for-scraping/) and create a DataFrame of food items from every restaurant. Your DataFrame should look something like this:

| restaurant | category | name    | calories | carbs | fat |
|------------|----------|---------|----------|-------|-----|
| McDonald's | Burgers  | Big Mac | 540      | 45    | 29  |
| Burger King | Burgers  | Whopper | 900      | 51    | 57  |
| ... | ...  | ... | ...      | ...    | ...  |
| Chili's | Ribs  | Shiner Bock® BBQ Ribs | 2310      | 168    | 123  |


**Note**: Your DataFrame should have just over 5,000 rows.

## Prerequisites

- Understand basic HTML
- Use inspect to interpret a website's HTML
- Use the `requests` and `BeautifulSoup` libraries