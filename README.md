# Netflix TV Shows and Movies EDA

This project explores the **Netflix TV Shows and Movies dataset** to perform **Exploratory Data Analysis (EDA)** using Apache Spark. The goal is to derive meaningful insights from the dataset and showcase the use of **PySpark** for big data processing.

## Project Overview

The Netflix dataset contains information about TV shows and movies available on the platform, including attributes like title, director, cast, country, release year, duration, and more. This project:

- Loads and preprocesses the Netflix dataset using **PySpark**.
- Performs various analytical tasks to derive insights, including:
  - Top directors by the number of titles.
  - Average release year by content type.
  - Duration analysis of content types.
  - Countries with the most diverse genres.
  - Titles with the longest words.
  - Distribution of content by rating.
  
The project demonstrates the power of Apache Spark in handling and analyzing large datasets.

## Dataset

- **Name**: Netflix TV Shows and Movies
- **Source**: [Netflix Titles Dataset on Kaggle](https://www.kaggle.com/datasets)
- **File Format**: CSV

### Attributes:
- **show_id**: Unique identifier for each show.
- **type**: Type of content (Movie or TV Show).
- **title**: Title of the content.
- **director**: Director of the content.
- **cast**: Cast members of the content.
- **country**: Country of production.
- **release_year**: Year of release.
- **duration**: Duration of the content.
- **rating**: Age rating of the content.
- **listed_in**: Genres of the content.

## Steps to Reproduce the Analysis

### 1. Prerequisites
- Docker installed on your system.
- Python 3.8+ installed locally (optional if running without Docker).

### 2. Set Up Environment

Clone the repository:

```bash
git clone https://github.com/your-username/netflix-eda.git
cd netflix-eda
docker build -t spark-py .

docker run -v $(pwd):/app -it spark-py

spark-submit /app/scripts/netflix_eda.py


