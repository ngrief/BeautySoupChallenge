# BeautySoupChallenge
# Mars Data Analysis

This repository contains two Python programs designed to scrape and analyze data from Mars-related web pages. The programs use tools such as `Splinter`, `BeautifulSoup`, `pandas`, and `matplotlib` to gather, process, and visualize data.

---

## Part 1: Mars News

### Purpose
The `part_1_mars_news.ipynb` notebook is designed to scrape the latest news articles from the Mars News website. It extracts the titles and preview text of the articles and organizes them into a structured format for further use.

### Steps
1. **Automated Browsing**:
   - Utilized `Splinter` to automate visiting the Mars News website.
   - Retrieved the HTML of the webpage for parsing.

2. **HTML Parsing**:
   - Used `BeautifulSoup` to parse the HTML and identify elements corresponding to the titles and preview text.
   - Located elements using class names such as `content_title` for titles and `article_teaser_body` for previews.

3. **Data Storage**:
   - Extracted the title and preview text for each article.
   - Stored the data in a list of dictionaries with keys: `title` and `preview`.

4. **Data Export**:
   - Optionally saved the scraped data to a JSON file for easy sharing and reusability.

### Key Libraries
- `Splinter`: Automates web browsing.
- `BeautifulSoup`: Parses and extracts data from HTML.
- `json`: Exports scraped data to a JSON file.

---

## Part 2: Mars Weather

### Purpose
The `part_2_mars_weather.ipynb` notebook is designed to scrape Mars weather data from a webpage containing an HTML table. The program organizes the data into a DataFrame, performs analysis, and visualizes key insights.

### Steps
1. **Automated Browsing**:
   - Used `Splinter` to visit the Mars Weather webpage.
   - Retrieved the HTML containing the weather data table.

2. **HTML Parsing**:
   - Leveraged `BeautifulSoup` to parse the HTML and locate the weather data table using its class name.

3. **Data Extraction**:
   - Extracted rows of data from the table.
   - Created a list of rows, ensuring non-empty rows were included.

4. **DataFrame Creation**:
   - Used `pandas` to construct a DataFrame from the extracted data.
   - Assigned appropriate column names, such as `id`, `terrestrial_date`, `sol`, `ls`, `month`, `min_temp`, and `pressure`.

5. **Data Cleaning and Conversion**:
   - Converted columns to appropriate data types (e.g., `datetime`, `int32`, `float64`).
   - Ensured consistency for further analysis.

6. **Analysis and Visualization**:
   - Identified the number of unique months and sols (Martian days).
   - Calculated averages for minimum temperature and atmospheric pressure by month.
   - Visualized key insights using bar charts and line plots.

7. **Data Export**:
   - Saved the cleaned and analyzed DataFrame to a CSV file in an `output` folder.

### Key Libraries
- `Splinter`: Automates web browsing.
- `BeautifulSoup`: Parses HTML and extracts tabular data.
- `pandas`: Organizes and processes data in a DataFrame.
- `matplotlib`: Visualizes data using bar charts and line plots.
- `os`: Creates output folders for saving files.

---

## Requirements
To run these programs, you need the following:
- Python 3.x
- Libraries:
  - `splinter`
  - `beautifulsoup4`
  - `pandas`
  - `matplotlib`

---

## Outputs
1. **Part 1: Mars News**:
   - JSON file containing the titles and previews of Mars news articles.

2. **Part 2: Mars Weather**:
   - CSV file (`mars_weather_data.csv`) containing the cleaned and analyzed Mars weather data.

---

## Insights
- The Mars News program enables easy access to the latest information from Mars-related missions.
- The Mars Weather program provides an in-depth analysis of Martian weather patterns, including temperature and atmospheric pressure variations.

---

## Usage
1. Clone the repository.
2. Run the notebooks in a Jupyter environment.
3. Ensure the required libraries are installed.
4. Review the JSON and CSV outputs for further exploration.

