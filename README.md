# Wikipedia Article Analysis Project

## Project Presentation

Check out my video explanation of this project and its results (in Hebrew):

[Project Overview Video](https://youtu.be/6e0ZFTIg_js)

## Overview

I often find myself falling down Wikipedia rabbit holes - you know, when you start reading about one topic and two hours later you're somehow reading about ancient civilizations or quantum physics. During these random adventures through Wikipedia articles, I noticed how some articles are available in tons of languages while others aren't. This got me wondering what makes certain articles more likely to be translated, so I decided to use data science to explore this question.
This project analyzes Wikipedia articles by collecting metadata through web scraping and applying various machine learning models to predict the number of languages an article is available in based on other article metrics.

## Features
- Web scraping of Wikipedia articles using randomized article selection
- Collection of multiple article metrics including:
  - Number of languages
  - Page views
  - Internal/external links
  - Edit statistics
  - Content metrics (characters, words, sections)
  - Redirect counts
- Data preprocessing and transformation
- Machine learning model implementation and comparison
- Visualization of data relationships and model performance

## Dependencies
```
pandas
matplotlib
numpy
seaborn
scikit-learn
requests
beautifulsoup4
tqdm
```

## Data Collection
The script collects data from Wikipedia using:
- Random article selection
- Automatic data saving every 1000 articles
- Rate limiting with random delays between requests

## Features Collected
- Topic (article title)
- Number of languages available
- Total page views
- Links from other articles
- Links to other articles
- External links
- Number of edits
- Number of unique editors
- Character count
- Word count
- Number of sections
- Number of redirects

## Data Preprocessing
1. Handling missing values (N/A replacement and removal)
2. Duplicate removal
3. Log transformation of numerical features
4. Data type conversion

## Analysis and Visualization
- Boxplots comparing features against number of languages
- Correlation heatmaps
- Feature distribution histograms
- Confusion matrices for model performance

## Machine Learning Models
Three classification models are implemented:
1. Random Forest Classifier
2. Naive Bayes Classifier
3. K-Nearest Neighbors (KNN)

Each model's performance is evaluated using:
- Accuracy score
- F1 score
- Confusion matrix (for Random Forest)

## Usage
1. Run the data collection script to gather Wikipedia article data:
```python
python wikipedia_scraper.py
```

2. The collected data will be saved to 'MyDataFrame.csv'

3. Run the analysis and modeling script:
```python
python analysis.py
```

## Future Improvements
- Implementation of more advanced ML models
- Feature engineering
- Hyperparameter tuning
- Extended error handling
- Additional data visualization options
