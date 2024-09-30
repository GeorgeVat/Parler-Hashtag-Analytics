# Parler Hashtags Analytics

This repository provides an analysis of the Parler social media platform, focusing on hashtags and their content from posts and comments collected between **October 1, 2020**, and **January 11, 2021**. The dataset coincides with key political events in the United States, including the presidential elections and the Capitol riot. By analyzing hashtags and user behavior on Parler, this project offers insights into the topics, discussions, and interests of the platform's users during that time.

## Project Overview

Given that Parler is a social network primarily associated with pro-Trump users and has not been extensively studied, this project aims to provide an analytical perspective of its content, specifically through hashtag analysis. The goal is to understand the nature of discussions, categorize them into relevant topics, and assess the toxicity of these conversations using natural language processing (NLP) techniques.

### Main Objectives

1. **Hashtag Extraction and Categorization:**
   - Extract all hashtags from posts and comments.
   - Clean the dataset by removing texts without any hashtags.
   - Create **four categories** of hashtags: `Trump`, `Conspiracy`, `Covid`, and `Biden` based on the content of the hashtags.
   - Analyze the most common hashtags within each category.

2. **Toxicity Analysis:**
   - Use the **Perspective API** to compute the toxicity levels of each post/comment. Toxicity here is defined as a measure of how likely a comment is to be considered offensive, insulting, or abusive.
   - Analyze the toxicity levels within each hashtag category to understand the sentiment and aggression levels in different topics of discussion.

3. **Top Users Analysis:**
   - Identify the users who contribute the most to each hashtag category.
   - Rank the top users based on the number of posts or comments they made within each category.

4. **Visualization:**
   - Generate **word clouds** to visualize the most common words in each hashtag category.
   - Plot the frequency of the top hashtags and visualize trends across different categories.

## Dataset

The dataset contains posts and comments from the Parler platform collected between October 1, 2020, and January 11, 2021. This period was chosen as it includes significant political events, such as the U.S. Presidential Elections and the Capitol Riot, which are expected to influence the topics of discussion on the platform.

### Data Preprocessing

- **Text Cleaning:** The dataset is cleaned by removing irrelevant characters, emojis, punctuation, and stop words.
- **Hashtag Extraction:** Hashtags are extracted from each post/comment. Only posts with at least one hashtag are retained for further analysis.
- **Categorization:** The extracted hashtags are grouped into four main categories:
  - **Trump Tags:** Hashtags related to Trump, his policies, and support for his presidency (e.g., `#trump`, `#maga`).
  - **Conspiracy Tags:** Hashtags associated with conspiracy theories, particularly around election fraud and anti-government sentiment (e.g., `#stopthesteal`, `#qanon`).
  - **Covid Tags:** Hashtags discussing the COVID-19 pandemic, vaccines, and related topics (e.g., `#covid`, `#coronavirus`).
  - **Biden Tags:** Hashtags related to Joe Biden, his policies, and opposition to his presidency (e.g., `#biden`, `#bidencrimefamily`).

## Methodology

### Toxicity Analysis

- The **Perspective API** is used to calculate toxicity levels for each post/comment. Toxicity is scored on a scale from 0 to 100, with higher scores indicating higher levels of offensive or harmful language.
- Posts with a toxicity score above **50** are considered extreme, and posts with scores above **85** are labeled as ultra-extreme.
- The toxicity distribution is analyzed for each hashtag category to understand the nature of the discussions.

### Top Users

- Users are ranked based on the number of posts/comments they made in each hashtag category.
- The top 15 most active users are identified for each category.

## Results and Visualizations

### Most Common Hashtags

For each of the four hashtag categories (`Trump`, `Conspiracy`, `Covid`, `Biden`), the most frequently used hashtags are extracted and visualized. Word clouds and bar plots show the top 100 hashtags in each category, highlighting the focus areas of Parler users during this period.

### Toxicity Levels

- **Trump Hashtags:**
  - Median Toxicity: 27.58%
  - Toxic Percentage (Toxicity > 50): 15.2%
  - Ultra Extreme Percentage (Toxicity > 85): 4.1%
  
- **Conspiracy Hashtags:**
  - Median Toxicity: 32.84%
  - Toxic Percentage: 18.3%
  - Ultra Extreme Percentage: 1.9%
  
- **Biden Hashtags:**
  - Median Toxicity: 42.89%
  - Toxic Percentage: 34.5%
  - Ultra Extreme Percentage: 7.7%
  
- **Covid Hashtags:**
  - Median Toxicity: 33.66%
  - Toxic Percentage: 22.75%
  - Ultra Extreme Percentage: 3.0%

These results indicate higher toxicity in discussions around Biden and conspiracy theories compared to Trump and Covid-related hashtags.

### Top Users

For each hashtag category, the users with the most posts/comments are identified and ranked. This analysis helps in understanding the most active contributors to the discussions around each topic on Parler.


## Conclusion

This project provides a comprehensive analysis of the content on Parler based on hashtags, offering insights into the dominant topics, the sentiment of discussions, and the activity of users on the platform. By categorizing hashtags into specific topics like Trump, conspiracy theories, Covid, and Biden, we gain a better understanding of the discourse during a highly politically charged period in U.S. history. The use of the Perspective API also helps measure the toxicity of these conversations, revealing the levels of offensive and harmful language across different topics.

Feel free to explore the code, modify it, and draw your conclusions from the dataset!
