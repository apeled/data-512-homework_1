# Wikipedia Article Traffic Analysis for Rare Diseases
### Author: Amit Peled

## Project Overview
This project analyzes monthly pageview traffic data for Wikipedia articles related to rare diseases, which we obtained from a subset of the "English Wikipedia that represents a large number of articles related to rare diseases. This list of pages was collected by using a database of rare diseases maintained by the [National Organization for Rare Diseases (NORD)](https://rarediseases.org) and matching them to Wikipedia articles that are either about a rare disease or have a section that mentions a rare disease." Data dates range from July 1, 2015, to September 30, 2024. The data is sourced from the [Wikimedia Analytics Pageviews API](https://www.mediawiki.org/wiki/Wikimedia_REST_API). The purpose of this analysis is to observe trends in article traffic over time, focusing on different access types: desktop, mobile-app, and mobile-web.

## Data Collection
* **API**: [Wikimedia Analytics Pageviews API](https://www.mediawiki.org/wiki/Wikimedia_REST_API)
* **Data**: Monthly pageviews for articles related to rare diseases
* **Access Types**: Desktop, mobile-app, mobile-web
* **Data Storage**: JSON files with time series data for each article in the specific subset
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
3. The analysis is performed within the notebook and visualized using `matplotlib`.

## License and Data Attribution
* The code in this repository is licensed under the MIT License.
* Data is sourced from the Wikimedia Analytics API, governed by the [Wikimedia Foundation Terms of Use](https://foundation.wikimedia.org/wiki/Terms_of_Use).
* This analysis abides by the guidelines outlined by the Wikimedia Foundation for data use in the link above.
