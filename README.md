# Indian Bike Market Analysis — Web Scraping and EDA

**An Exploratory Data Analysis project using web scraping to analyse bike prices, technical specifications, and brand representation in India.**

## 📌 Project Overview

Choosing a suitable bike can be challenging because models differ in price, mileage, engine capacity, power, weight, and user ratings. Comparing these features manually across multiple product pages can be time-consuming.

This project collects bike information from [BikeWale](https://www.bikewale.com/) using Python web scraping techniques and analyses the collected data using Exploratory Data Analysis (EDA).

The project aims to understand patterns in bike specifications, explore relationships between important features, and support comparisons based on different buyer priorities, such as affordability, mileage, and performance.

## 🎯 Objectives

- Collect bike specifications from BikeWale product pages.
- Extract and organise relevant information into a structured dataset.
- Clean the collected data and examine missing values and duplicates.
- Analyse price, mileage, engine capacity, power, and brand representation.
- Explore relationships between price and technical specifications.
- Use correlation analysis and summary tables to identify patterns.
- Compare bikes according to different buyer requirements.
- Document the limitations of the scraped dataset and the analysis.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Data collection, cleaning, and analysis |
| Requests | Retrieve webpage HTML |
| BeautifulSoup | Parse HTML content |
| Regular Expressions | Extract relevant values from text |
| Pandas | Data manipulation and analysis |
| Matplotlib | Data visualisation |
| Seaborn | Statistical plots and correlation heatmaps |
| Jupyter Notebook | Development and execution environment |

## 🌐 Data Source

**Website:** [BikeWale](https://www.bikewale.com/)

The project uses publicly accessible BikeWale product pages as its data source. The collected information includes bike names, source URLs, starting prices, engine capacity, mileage, power, weight, and user ratings where available.

The dataset represents the records collected for this project and should not be considered a complete representation of the Indian two-wheeler market.

## 📊 Dataset Description

The cleaned dataset contains **65 bike records across 22 brands**.

| Dataset Information | Value |
|---|---:|
| Cleaned records | 65 |
| Brands represented | 22 |
| Electric records | 11 |
| Petrol/Other records | 54 |
| Dataset columns | 14 |

### Key Features

- **Bike Name:** Name of the bike model.
- **URL:** Source webpage for the record.
- **Starting Price:** Listed starting price in Indian rupees.
- **Engine Capacity (CC):** Engine displacement, where applicable.
- **Mileage (KMPL):** Reported fuel efficiency, where applicable.
- **Maximum Power (BHP):** Reported power output.
- **Kerb Weight (KG):** Bike weight in kilograms.
- **User Rating:** User rating, where available.
- **Number of Ratings:** Number of user ratings, where available.

Additional columns may contain brand information, bike classification, or data-quality information.

## ⚙️ Project Workflow

### 1. Web Scraping

- Retrieved webpage HTML using Requests.
- Parsed webpage content using BeautifulSoup.
- Extracted relevant bike details using text processing and regular expressions.
- Retained source URLs to support later verification.

### 2. Data Cleaning

- Inspected the dataset structure and column types.
- Converted relevant price and technical specification fields into numeric values.
- Checked for duplicate records.
- Identified missing specifications.
- Flagged suspicious model names and extracted values for verification.
- Avoided automatically replacing unavailable specifications with zero.

### 3. Univariate Analysis

Examined individual variables using histograms and bar charts, including:

- Bike price distribution.
- Mileage distribution.
- Engine capacity distribution.
- Lowest-priced bikes in the sample.
- Number of records by brand.

### 4. Bivariate Analysis

Used scatter plots to explore relationships between:

- Engine capacity and price.
- Power and price.
- Mileage and price.

### 5. Multivariate Analysis

Created a correlation heatmap to examine relationships among numerical features, including price, engine capacity, mileage, power, and weight.

### 6. Summary and Insights

Compared average prices by bike type and examined brand representation and other group-level patterns using summary tables and pivot-table analysis.

## 🔍 Key Findings

The current analysis of the collected sample indicates the following patterns:

- Bike prices are right-skewed, with most records concentrated in lower price ranges and a small number of premium models extending the distribution.
- Price shows a positive association with engine capacity and power.
- Mileage shows a negative association with price in the available sample.
- Engine capacity and power are strongly positively correlated in the available records.
- Brand counts show how the scraped records are distributed across manufacturers.
- Electric and petrol bikes require different comparison criteria because their powertrain specifications differ.

The strength of these relationships depends on the available observations, missing values, and accuracy of the extracted specifications. Correlation indicates association, not causation.

## 📈 Visualisations

The project includes:

- Price distribution histogram.
- Lowest-priced bike comparison.
- Brand-count bar chart.
- Mileage distribution histogram.
- Engine capacity distribution histogram.
- Engine capacity versus price scatter plot.
- Power versus price scatter plot.
- Mileage versus price scatter plot.
- Correlation heatmap.
- Average price comparison by bike type.

These visualisations help identify patterns, compare features, and communicate the results of the analysis.

## 🧹 Missing Values and Data Quality

Some bike specifications were unavailable or could not be reliably extracted from the source pages.

The cleaned dataset contains missing values in several technical specification columns. Missing values were retained where reliable replacements were unavailable rather than being automatically treated as zero.

Some model names and specifications also require source verification. Consequently, individual model recommendations should be made only after checking the relevant source information.

## ⚠️ Limitations

- The dataset contains a limited sample of 65 records and does not cover every bike available in India.
- Missing specifications reduce the number of observations available for some analyses.
- Webpage layouts and extracted text may cause scraping errors.
- Some model names and specifications require additional verification.
- Average prices and correlations may be influenced by premium models and the composition of the sample.
- User ratings and other specifications may change over time.
- The analysis does not establish one universally best bike for every buyer.

## 🚀 How to Run the Project

1. Clone or download this repository.
2. Install Python and Jupyter Notebook.
3. Install the required libraries:

   ```bash
   pip install requests beautifulsoup4 pandas matplotlib seaborn
   ```

4. Open the project notebook:

   ```bash
   jupyter notebook
   ```

5. Open `web scrapping bikewale.ipynb`.
6. Run the notebook cells in sequence.

**Note:** The scraping process depends on the availability and structure of the source webpages. If you rerun the notebook, the collected records and resulting statistics may differ from the current dataset.

## 📁 Repository Contents

- `web scrapping bikewale.ipynb` — web scraping and analysis notebook.
- `bikewale_raw_dataset.csv` — raw scraped dataset.
- `bikewale_cleaned_dataset.csv` — cleaned dataset used for analysis.
- `bikewale_validated_working_dataset.csv` — working dataset with validation-related changes.
- `bikewale_correlation_matrix.csv` — correlation results.
- `bikewale_outlier_analysis.csv` — outlier analysis results.
- `bikewale_pivot_table.csv` — summary and pivot-table results.
- `bikewale_scraping_errors.csv` — scraping error log.

## 🔮 Future Improvements

- Verify all model names and specifications against their source pages.
- Improve extraction reliability using structured webpage data where available.
- Expand the dataset to include more models and brands.
- Collect electric-specific features such as battery capacity and claimed range.
- Add more robust data validation and automated cleaning.
- Develop a transparent feature-based ranking system for different buyer priorities.
- Build an interactive dashboard to explore bike specifications and comparisons.

## 👨‍💻 Author

**Appaji Sree Dharma Shasta Rao**  
B.Tech — Computer Science and Engineering, Artificial Intelligence and Machine Learning

- GitHub: [Appajisdsrao](https://github.com/Appajisdsrao)
- LinkedIn: [Connect on LinkedIn](https://www.linkedin.com/in/appaji-sree-dharma-shasta-rao-33133129b/)

## 📄 Disclaimer

This project is intended for educational and analytical purposes. BikeWale is the source of the collected product information. This repository is not affiliated with or endorsed by BikeWale. Prices, ratings, and specifications may change, and the analysis should be interpreted in the context of the collected sample.

---

**If you find this project useful, consider starring the repository!**
