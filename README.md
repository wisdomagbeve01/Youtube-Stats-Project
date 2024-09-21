# Project Overview

## Table of Contents

- [Project Overview](#project-overview)
- [Data Description](#data-description)
- [Tools Used](#tools-used)
- [Data Cleaning](#data-cleaning)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Key Metrics Measured](#key-metrics-measured)
- [Visualizations](#visualizations)
- [Results](#results)
- [Limitations](#limitations)
- [Recommendations](#recommendations)
- [References](#references)

## Project Overview

This project analyzes the Global YouTube Statistics dataset, sourced from Kaggle, which provides a rich collection of data on top YouTube creators. The dataset includes information such as subscriber counts, video views, upload frequency, country of origin, and estimated earnings. The primary goal of this analysis is to gain insights into the YouTube landscape by examining key trends, such as which continents are home to the most successful YouTubers and other important patterns. Through data visualization and statistical methods, this project aims to provide a clearer understanding of the global reach and influence of YouTube creators, making it valuable for data enthusiasts, aspiring content creators, and anyone curious about the dynamics of the platform.

## Data Source

`Kaggle`

## Data Description

The Global YouTube Statistics dataset contains detailed information about top YouTube creators. The dataset used is the [Global YouTube Statistics 2023](https://www.kaggle.com/datasets/nelgiriyewithana/global-youtube-statistics-2023). The key fields in the dataset include:

- **Creator Name:** The name of the YouTube channel or creator.
- **Subscriber Count:** The number of subscribers each creator has, indicating their audience size.
- **Video Views:** Total views accumulated across all videos on the channel, representing the level of content consumption.
- **Upload Frequency:** The number of videos the creator has uploaded, providing insight into their activity and consistency on the platform.
- **Country of Origin:** The country where the creator is based, allowing for geographic analysis of YouTube trends.
- **Estimated Earnings:** The estimated revenue generated by the creator from their YouTube content, which reflects their financial success.


## Tools Used

1. **Python:** The primary programming language used for data manipulation and analysis.
2. **Pandas:** A library for data cleaning, manipulation, and exploration, facilitating tasks like handling missing values, generating summaries, and modifying data types.
3. **NumPy:** A library for efficient numerical computing, used to support array-based operations.
4. **Seaborn/Matplotlib:** Libraries used to create visualizations such as plots and graphs to identify trends and patterns in the data.
5. **MySQL:** The SQL database used for querying and generating descriptive statistics directly from the dataset.
6. **Google Colab:** The cloud-based platform where the analysis was performed, enabling interactive exploration and visualization.

## Data Cleaning

The data cleaning and preparation process involved the following steps:

1. **Initial Exploration:**
 - Checked the shape of the dataset and used the `.info()` function to get an overview of the dataset’s structure, including data types and non-null values.
2. **Summary Statistics:**
  - Generated a statistical summary using the `.describe()` command in SQL to understand key metrics such as counts, means, and standard deviations for numerical columns
3. **Handling Unnecessary Columns:**
- Identified and dropped six columns that were not relevant to the analysis: `Gross tertiary education enrollment (%)`, `Population`, `Unemployment rate`, `Urban_population`, `Latitude`, `Longitude`, and `subscribers_for_last_30_days`.
4. **Missing Values Treatment:**
- Replaced missing values in the `Abbreviation` and `channel_type` columns with "Not available" to ensure consistent data.
- For `channel_type_rank` and `country_rank`, missing values were replaced with the mode (the most frequent value), as these are categorical rankings.
5. **Final Missing Values Check:**
- Rechecked for any remaining missing values and chose to drop rows with missing values in `created_month` and `created_date` since the number of missing entries was minimal and wouldn't impact the analysis.
6. **Data Type Adjustments:**
- Converted date columns from float values to a proper date-type format to enable better handling of time-based analysis.

## Exploratory Data Analysis

During the EDA phase, several key questions were addressed to explore and understand the dataset:

1. What YouTube category has the most activity?
2. What countries have the highest amount of YouTube activity?
3. What continents have the highest amount of YouTube activity?
4. What is the relationship between uploads and subscribers?
5. What is the relationship between subrscribers and earnings at different continents?

## Key Metrics Measured
`Subscriber Count`, `Video Views`, `Upload Frequency`, `Country of Origin`, `Channel Type`, `Estimated Earnings`, `Channel and Country Rank`

## Visualizations

1. **Bar Chart of YouTube Categories by Activity**
<img width="848" alt="Screenshot 2024-09-20 at 11 02 50 PM" src="https://github.com/user-attachments/assets/e6d773d5-2e06-4c83-a9ff-6b9f1fea4267">

This chart highlights which content genres (e.g., entertainment, gaming, education) have the most uploads, providing a clear picture of where creators are most active on the platform. By plotting the number of videos uploaded within each category, the bar chart allows for an easy comparison of the popularity and engagement of different types of content.
This visualization helps in understanding the distribution of activity across various content genres and offers insights into which areas of YouTube are most saturated or growing rapidly.

2. **Bar Chart of Countries by YouTube Activity**
<img width="833" alt="2" src="https://github.com/user-attachments/assets/34da21d2-d3b2-47fe-b76c-82ec544c1620">

This chart presents the total number of uploads from creators based in different countries, highlighting which regions are most active on the platform. By comparing the volume of uploads from various countries, this bar chart provides insights into geographic trends in YouTube content creation.
This visualization helps identify the countries that dominate the platform in terms of creator activity and can offer a deeper understanding of regional trends and preferences in online content.


