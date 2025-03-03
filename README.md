# NBA Odds Scraper

This project is a web scraper that extracts NBA match results and betting odds from Flashscore using Selenium and stores the data in a CSV file.

## Features
- Extracts match details such as date, teams, scores, and betting odds from Bet365.
- Saves the extracted data into a CSV file (`nba_bet365_odds.csv`).
- Uses Selenium to automate data retrieval and page navigation.
- Runs in headless mode for efficiency.

## Requirements

Ensure you have the following installed:
- Python 3.x
- Google Chrome
- ChromeDriver (ensure it matches your Chrome version)
- Required Python libraries:
  ```bash
  pip install selenium pandas
  ```

## Setup
1. Download and install [ChromeDriver](https://sites.google.com/chromium.org/driver/).
2. Update the script with the correct path to your `chromedriver.exe`:
   ```python
   service = Service('path to chromedriver')
   ```
3. Run the script:
   ```bash
   python nba_scrapper.py
   ```
4. The extracted data will be saved in `nba_bet365_odds.csv`.

## How It Works
- The script navigates to Flashscore's NBA results page.
- It scrolls down to load more results.
- Extracts match details and constructs summary URLs.
- Opens match summary pages to extract Bet365 odds.
- Saves the collected data into a CSV file.

## Notes
- The script runs in headless mode, so no browser window will appear.
- It waits for elements to load to avoid missing data.
- The script currently processes only the first three matches for testing purposes.

## License
This project is licensed under the MIT License.

## Disclaimer
This project is for educational purposes only. Flashscore's terms of service should be reviewed before using this scraper for commercial purposes.

