# Wikipedia Scraper
### BeCode - Data Science and AI Bootcamp - Project 2

This project fetches data about country leaders from https://country-leaders.onrender.com, fetches, cleans and adds a short introductory paragraph for each leader from their respective Wikipedia page.

The final dictionary data is then saved in JSON format for easy access and later use. The content of the output file is then reloaded and checked and a message confirms, if the execution has been successful.


## Project Structure
* `leaders_scraper.py`: The main script file that:
  * Fetches country and leader data from the API and stores in a dictionary
  * Retrieves and cleans the first paragraph of the Wikipedia article for each country leader and adds paragraph to the dictionary
  * Saves the data in a `leaders.json` file
* `wikipedia_scraper.ipynb`: The instructions and tasks for the project.

## Features
1. **API Data Retrieval:** The script connects to an API that provides information about country leaders, organized by country.
2. **Wikipedia Data Scraping and Cleaning:** For each leader, the script uses a session to retrieve and clean the first paragraph from their Wikipedia page.
3. **JSON Output:** The final data, in the format of a dictionary, organized by country and including the respective Wikipedia snippets, is saved as a JSON file.

## Usage

Run the script to fetch data about country leaders, retrieve a short Wikipedia introduction and save everything to a JSON file:

* For Windows:

  ```python 
  python leaders_scraper.py
  ```
* For Linux:
  ```python
  python3 leaders_scraper.py 
  ```

## Code Overview - Main Functions

* `get_leaders()`: Retrieves the data of country leaders from the API, gets Wikipedia paragraphs, and saves everything to a dictionary.
* `get_first_paragraph(wikipedia_url, session)`: Fetches and cleans the first paragraph from the country leaders' Wikipedia page using a session.
* `save(leaders_per_country)`: Saves the collected country leader data including the Wikipedia paragraph to a JSON file.