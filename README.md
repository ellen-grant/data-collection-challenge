# Mars Weather Data Scraping and Analysis

## Overview
This project involves scraping data related to weather on Mars, specifically from the Curiosity Rover's data. The project collects, organizes, and analyzes the atmospheric and temperature data on Mars using web scraping techniques with Splinter and BeautifulSoup. Data is then analyzed using Pandas to identify patterns, such as the coldest and warmest months on Mars, the months with the lowest and highest atmospheric pressure, and the length of a Martian year in terms of Earth days.

## Project Structure

The project consists of two main parts:
1. Mars News Scraping: Scrapes news titles and preview text from a Mars-related news site.
2. Mars Weather Scraping and Analysis: Scrapes and analyzes atmospheric and temperature data from a table on the Mars Facts website.

## Deliverables
1. Deliverable 1: Scrape Titles and Preview Text from Mars News
  - This part involves scraping Mars news articles, including the title and preview text, from a designated website.
  - The scraped data is stored in a list of dictionaries and printed for review.
2. Deliverable 2: Scrape and Analyze Mars Weather Data
  - This part involves scraping Mars weather data from an HTML table and analyzing it to answer specific questions.
  - The data is organized into a Pandas DataFrame, and various calculations and visualizations are performed to understand Martian weather patterns.

## Technologies Used
- Python: Programming language used to implement the project.
- Jupyter Notebook: Used for running Python code interactively and displaying results.
- Splinter: A Python library used for automated web browsing.
- BeautifulSoup: A library for web scraping to extract data from HTML and XML files.
- Pandas: A Python library used for data manipulation and analysis.
- Matplotlib: Used for data visualization and plotting graphs.
- ChromeDriver: Used in conjunction with Splinter for automated browsing.

## Data Scraping Steps
### Part 1: Scrape Mars News
1. Automated browsing: Splinter is used to open the Mars news website.
2. Scraping: Using BeautifulSoup, the script identifies and extracts the titles and preview texts of the news articles on the website.
3. Data storage: The scraped data is stored in a list of dictionaries, where each dictionary contains two keys:
  - title: The news article title.
  - preview: A short preview text of the article.

### Part 2: Scrape and Analyze Mars Weather Data
1. Automated browsing: Splinter is used to open the Mars weather data site.
2. Scraping: BeautifulSoup extracts the data from the HTML table, including:
  - id: Identification number of the transmission from the Curiosity Rover.
  - terrestrial_date: The date of the observation in Earth days.
  - sol: The number of Martian days since the Curiosity rover landed on Mars.
  - ls: The solar longitude of Mars.
  - month: The Martian month (1-12).
  - min_temp: Minimum temperature in Celsius.
  - pressure: Atmospheric pressure at the rover’s location.
3. Data organization: The extracted data is stored in a Pandas DataFrame for further analysis.

## Analysis and Results
### 1. Number of Months on Mars
- Result: There are 12 months on Mars, similar to Earth, though the length of each month varies due to Mars’ orbital characteristics.
### 2. Number of Sols (Martian Days) in the Data
- Result: The dataset contains observations spanning over a certain number of Martian days (sols). This count is obtained using Pandas to calculate the unique number of sols.
### 3. Coldest and Warmest Months
- Result: The coldest month has an average minimum temperature of around -80°C, while the warmest month has an average minimum temperature of around -65°C. This is analyzed by grouping the data by month and averaging the minimum temperatures.
### 4. Atmospheric Pressure Variations
- Result: The lowest atmospheric pressure occurs in Month 6, while the highest pressure occurs in Month 9. These variations are visualized using a bar chart to show the average pressure by month.
### 5. Length of a Martian Year
- Result: By analyzing the periodicity of temperature fluctuations, the length of a Martian year is estimated to be approximately 687 Earth days. This matches with known scientific data on Mars' orbit.

## How to Run the Project
### Prerequisites
Make sure you have the following installed:
  - Python (3.7 or higher)
  - Jupyter Notebook
  - ChromeDriver (for automated browsing)
  - Required Python libraries: Splinter, BeautifulSoup, Pandas, Matplotlib

### Steps
1. Clone the repository (if using version control) or download the project files.
2. Run Jupyter Notebook:
  - Open the project in Jupyter Notebook and execute the cells step by step.
3. Export the Data

### File Structure
mars_weather_scraping/

│

├── part_1_mars_news.ipynb          # Jupyter notebook for Mars news scraping

├── part_2_mars_weather.ipynb       # Jupyter notebook for Mars weather scraping and analysis

├── README.md                       # Project readme file

└── mars_weather_data.csv           # CSV file containing the scraped Mars weather data

## Future Improvements
- Dynamic Website Scraping: Currently, the project uses static HTML content. Implementing dynamic scraping for real-time data updates could enhance the project.
- Machine Learning Analysis: Further data analysis using machine learning could reveal deeper patterns in the Martian weather and predict trends.
- Automated Scheduling: Set up the scraping process to run at regular intervals to collect more recent data.

## Refernces
The Mars News website is operated by edX Boot Camps LLC for educational purposes only. The news article titles, summaries, dates, and images were scraped from NASA's Mars News website in November 2022. Images are used according to the JPL Image Use Policy, courtesy NASA/JPL-Caltech.
