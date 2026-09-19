# Netflix Data Analysis

## Overview

This project performs exploratory data analysis (EDA) on the Netflix Titles dataset to identify patterns and trends across movies and TV shows.

The analysis focuses on content distribution, title additions over time, release-to-platform gaps, movie duration, ratings, countries, and genres. The project demonstrates practical data cleaning, transformation, feature engineering, statistical analysis, and visualization using Python.

## Objectives

- Understand the composition of the Netflix content catalog represented in the dataset.
- Analyze the distribution of Movies and TV Shows.
- Examine how the number of titles added to the dataset changed over time.
- Compare Movies and TV Shows across different years.
- Analyze the relationship between a title's release year and its Netflix addition year.
- Study the distribution of movie durations.
- Identify commonly occurring ratings, countries, and genres.
- Develop practical experience with exploratory data analysis and data visualization.

## Dataset

The dataset contains 8,807 Netflix titles and includes the following attributes:

| Column | Description |
|---|---|
| `show_id` | Unique identifier for each title |
| `type` | Movie or TV Show |
| `title` | Title name |
| `director` | Director of the title |
| `cast` | Cast members |
| `country` | Country or countries associated with the title |
| `date_added` | Date the title was added to Netflix |
| `release_year` | Original release year |
| `rating` | Content rating |
| `duration` | Movie duration or number of TV seasons |
| `listed_in` | Genres and categories |
| `description` | Title description |

## Technologies and Tools

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook
- Git
- GitHub

## Project Structure

```text
Netflix-Data-Analysis/
│
├── data/
│   └── netflix_titles.csv
│
├── notebooks/
│   └── netflix_analysis.ipynb
│
├── visualizations/
│   ├── movies_vs_tv_shows.png
│   ├── titles_added_by_year.png
│   ├── movies_vs_tv_shows_over_time.png
│   ├── years_to_add_distribution.png
│   ├── movies_duration_distribution.png
│   ├── movie_ratings.png
│   ├── top_10_countries.png
│   └── top_10_genres.png
│
├── .gitignore
├── README.md
└── requirements.txt
Data Cleaning and Preparation

The dataset was inspected for missing values, data types, and formatting inconsistencies.

The following preprocessing steps were performed:

Identified missing values across relevant columns.
Handled missing categorical values using appropriate placeholder values.
Converted date_added from string format to datetime.
Extracted the year from date_added for time-based analysis.
Filtered movie records for movie-specific analysis.
Extracted numeric movie durations from values such as "90 min".
Created a derived years_to_add feature to estimate the year-level difference between a title's release year and its Netflix addition year.
Excluded negative year gaps from the specific gap-distribution analysis without modifying the original dataset.
Exploratory Data Analysis
1. Movies vs TV Shows

The dataset contains:

6,131 Movies
2,676 TV Shows

Movies account for approximately 69.6% of the titles, while TV Shows account for approximately 30.4%.

2. Titles Added by Year

The number of titles represented in the dataset increased substantially from 2015 onward, reaching a peak of 2,016 titles in 2019.

3. Movies vs TV Shows Over Time

Movies remained the larger category across most years represented in the dataset. The proportion of TV Shows increased in the later years.

4. Release Year vs Date Added

A years_to_add feature was created using:

years_to_add = date_added_year - release_year

The distribution is concentrated around smaller gaps. The most common non-negative gap is 0 years, followed by 1 year.

5. Movie Duration

For movie-specific analysis, numeric durations were extracted from the duration column.

Key statistics:

Statistic	Duration
Mean	99.58 minutes
Median	98 minutes
25th Percentile	87 minutes
75th Percentile	114 minutes
Minimum	3 minutes
Maximum	312 minutes

The middle 50% of movies have durations between 87 and 114 minutes.

6. Movie Ratings

The distribution of content ratings was analyzed to identify the most frequently occurring rating categories among movies.

7. Countries

Country information was split and expanded to identify the countries most frequently associated with titles in the dataset.

8. Genres

The listed_in column was split and expanded to identify the most frequently occurring genres and categories.

Key Findings
Movies represent approximately 69.6% of the titles in the dataset.
The number of titles added increased substantially during the late 2010s.
2019 had the highest number of title additions in the dataset.
Movies generally have a duration close to 100 minutes.
The median movie duration is 98 minutes.
The dataset contains titles associated with a wide range of countries and genres.
Many titles have a small year-level gap between their recorded release year and Netflix addition year.
Limitations

The analysis describes the provided dataset and should not be interpreted as a complete representation of Netflix's global catalog.

Some limitations include:

The dataset may not represent the current Netflix catalog.
date_added contains missing values.
country and listed_in can contain multiple values within a single record.
release_year provides only the year rather than an exact release date.
The years_to_add calculation is therefore an approximate year-level measure.
Some metadata inconsistencies can produce negative year gaps.
Country information represents countries associated with titles and should not necessarily be interpreted as production volume.
Conclusion

This project demonstrates an end-to-end exploratory data analysis workflow using a real-world entertainment dataset. It covers data inspection, missing-value handling, data transformation, feature engineering, descriptive statistics, and visualization.

The analysis provides a structured view of content types, temporal trends, movie characteristics, ratings, geographic representation, and genre distribution within the dataset.

Author

Minakshi Kaushik

B.Tech Computer Science and Engineering
Indira Gandhi Delhi Technical University for Women

GitHub: Minakshi-kaushik