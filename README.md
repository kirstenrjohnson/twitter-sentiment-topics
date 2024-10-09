# twitter-sentiment-topics
## Project Overview

This project conducts topic modeling and sentiment analysis on tweets mentioning MassDOT, the Massachusetts Department of Transportation. With recent public dissatisfaction surrounding transportation in Massachusetts, particularly the MBTA, this analysis aims to explore whether a negative sentiment can be identified towards MassDOT and to provide insights into frequent topics related to the agency.

Although the MBTA and MassDOT are separate agencies, they are often conflated in public discourse. By analyzing Twitter data, I aim to identify frequent topics, understand how these topics relate to one another, and determine the overall sentiment expressed in these discussions.

Goals:
Identify frequent topics related to MassDOT on Twitter.
Analyze the relationship between these topics to gain insight into public discourse.
Determine the sentiment surrounding these topics.
## Data Collection
I used the twarc2 package to scrape tweets mentioning MassDOT from the past month. These tweets were saved in a CSV format for further analysis.

## Preprocessing Steps

To prepare the data for analysis, the following preprocessing steps were conducted:

Removal of usernames, hashtags, URLs, numbers, and special characters.
Conversion of text to lowercase.
Removal of tweets with fewer than 3 words.
Lemmatization of words to their root forms.
Tokenization and removal of stopwords.
## Topic Modeling

Latent Dirichlet Allocation (LDA) was used to model the topics within the tweets. I experimented with different models ranging from 4 to 8 topics. The model with 5 topics was selected as the most optimal, providing distinct yet meaningful topic groupings.

## Sentiment Analysis

Sentiment analysis was conducted to determine the overall tone of the tweets related to MassDOT. This analysis helped identify whether the discourse was generally positive, negative, or neutral.

## Repository Contents

data/: Contains the raw Twitter data csv.
scripts/: Includes the R scripts used for data preprocessing, topic modeling, and sentiment analysis.
results/: Contains the LDA model results, visualizations, and sentiment analysis outputs in poster format.
README.md: This file, providing an overview of the project and its contents.
## Tools & Libraries Used
-R programming language
-`twarc2` (for data collection)
-`tidyverse`, `quanteda`, `tidytext`, `text2vec` (for data preprocessing and text analysis)
-`LDAvis` (for topic modeling visualization)
-`textstem` (for lemmatization)
-`syuzhet` (for sentiment analysis)
## Instructions for Running the Project

Clone the repository.
Install the required R packages:
R
Copy code
packages <- c("cleanNLP", "devtools", "tidytext", "plyr", "tidyverse", "quanteda", "wordcloud", "syuzhet","wordcloud2", "text2vec")
install.packages(setdiff(packages, rownames(installed.packages())))

Run the preprocessing and analysis scripts in the scripts/ directory to replicate the results.
