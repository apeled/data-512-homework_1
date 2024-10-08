# Wikipedia Article Traffic Analysis for Rare Diseases
### Author: Amit Peled

## Project Overview
This project analyzes monthly pageview traffic data for Wikipedia articles related to rare diseases, which we obtained from a subset of the "English Wikipedia that represents a large number of articles related to rare diseases. This list of pages was collected by using a database of rare diseases maintained by the [National Organization for Rare Diseases (NORD)](https://rarediseases.org) and matching them to Wikipedia articles that are either about a rare disease or have a section that mentions a rare disease." These are found in the CSV file provided by the instructors of the class in this repository `rare-disease_cleaned.AUG.2024.csv`. Data dates range from July 1, 2015, to September 30, 2024. The data is sourced from the [Wikimedia Analytics Pageviews API](https://doc.wikimedia.org/generated-data-platform/aqs/analytics-api/reference/page-views.html). The purpose of this analysis is to observe trends in article traffic over time, focusing on different access types: desktop, mobile-app, and mobile-web.

## Data Collection
* **API**: [Wikimedia Analytics Pageviews API](https://doc.wikimedia.org/generated-data-platform/aqs/analytics-api/reference/page-views.html)
* **Data**: Monthly pageviews for articles related to rare diseases. Each record in the JSON files includes:
  * `project`: The project name (e.g., "en.wikipedia").
  * `article`: The article title.
  * `granularity`: Set to "monthly".
  * `timestamp`: The month for the pageviews.
  * `agent`: The type of agent (e.g., "user").
  * `views`: The number of pageviews for the month.
* **Access Types**: Desktop, mobile-app, mobile-web
* **Data Storage**: The data is saved in JSON files with time series data for each article:
  * `rare-disease_monthly_mobile_201507-202409.json`
  * `rare-disease_monthly_desktop_201507-202409.json`
  * `rare-disease_monthly_cumulative_201507-202409.json`

## Analysis
1. **Maximum and Minimum Average Page Views**: Graph of the time series for articles with the highest and lowest average monthly page views for both mobile and desktop.
2. **Top 10 Peak Page Views**: Graph of the time series of articles with the highest peak page views over the entire period for both mobile and desktop.
3. **Fewest Months of Data**: Graph of the articles with the fewest months of available data for both mobile and desktop.

## Files
* **Data Files**:
  - JSON files containing the collected data in time series format.
* **Notebook**:
  - Contains code for data acquisition, processing, and analysis with explanations in Markdown.
* **License**:
  - MIT License for the project's code.
* **Images**:
  - PNG files of the final visualizations.

## How to Reproduce the Analysis
1. Install necessary libraries: `requests`, `pandas`, `matplotlib`.
2. Run the notebook to acquire the data using the Wikimedia Analytics API. Or use the pre-loaded data found within the repository.
- You can find the collected data in the following JSON files:
     - `rare-disease_monthly_mobile_201507-202409.json`
     - `rare-disease_monthly_desktop_201507-202409.json`
     - `rare-disease_monthly_cumulative_201507-202409.json`
4. The analysis is performed within the notebook and visualized using `matplotlib`.

## License and Data Attribution
* The code in this repository is licensed under the MIT License.
* Data is sourced from the [Wikimedia Analytics API](https://www.mediawiki.org/wiki/Wikimedia_REST_API), and the subset of rare diseases is based on the [National Organization for Rare Diseases (NORD)](https://rarediseases.org) database.
* The data use adheres to the [Wikimedia Foundation Terms of Use](https://foundation.wikimedia.org/wiki/Terms_of_Use).

## Acknowledgments
This project built upon the sample code developed by Dr. David W. McDonald for use in DATA 512, a course in the UW MS Data Science degree program. This code is provided under the [Creative Commons CC-BY license](https://creativecommons.org/).

This project was developed with the assistance of [ChatGPT](https://openai.com/chatgpt), which helped format code, structure the README, and organize the data and analysis in an efficient and clear manner. All content has been verified and tested by the author.

## Known Issues or Limitations
* **API Rate Limits**: The Wikimedia Analytics Pageviews API has rate limits that may affect large-scale data requests. We handle this by adding a delay between requests, but future users should be aware.
* **Missing Data**: Some articles may have missing data for certain months. This can result in shorter time series for some articles.


