# Automated-Wikipedia-See-Also-Section-Generation

This project automates the creation and updating of "See Also" sections in Wikipedia articles using NLP-generated semantic vectors and article features. It was submitted for the Data Science Group Project Module at the University of Birmingham. Contributors to this project include Kenya Williams, Mohammad Hijjawi, Swapnil Bhattacharya, and Richmond Boakye.

## Introduction

The goal of this project is to improve the relevance and ease of navigation across Wikipedia articles by automating the "See Also" sections. Our system leverages advanced Natural Language Processing (NLP) techniques and semantic vector analysis to generate recommendations that are both contextually relevant and valuable to readers.

## Project Goals

- **Automate "See Also" Section Creation**: Develop a system that can automatically generate "See Also" sections for Wikipedia articles.
- **Utilize NLP and Article Features**: Combine article-specific features with NLP-generated semantic vectors to improve link relevance.
- **Improve Wikipedia Navigation**: Enhance the connectivity between articles to facilitate easier navigation for Wikipedia users.

## Approach

### Data Collection and Preparation

1. **Article Selection**:
    - Selected the top 60,000 most-clicked English Wikipedia articles based on clickstream data.
    - This selection ensures the dataset is highly relevant and manageable within our computational constraints.

2. **Feature Extraction**:
    - Extracted various features from the selected articles including titles, introductions, categories, size, quality, and view counts.
    - Used web scraping and APIs to gather necessary data.

### NLP Model Selection

1. **Model Evaluation**:
    - Evaluated multiple NLP models such as BERT, GPT, RoBERTa, and others for generating semantic vectors.
    - Chose BERT for its superior contextual understanding and semantic similarity capabilities.

### Semantic Vector Generation

1. **Text Processing**:
    - Combined article titles, introductions, and categories into a single string for each article.
    - Generated semantic vectors using BERT to capture the contextual meaning of each article.

2. **Similarity Calculation**:
    - Used cosine similarity to measure the relevance between articles based on their semantic vectors.
    - This metric ensures that recommendations are based on content similarity regardless of article length.

### Recommendation System

1. **Filtering**:
    - Excluded articles with insufficient content (less than 6,000 bytes) to ensure recommendations are substantial.
    - Selected the top 20 articles with the highest cosine similarity scores.

2. **Ranking**:
    - Sorted the top 20 articles by the number of shared categories with the input article.
    - Further refined the selection to the top 10 articles based on total views and quality scores.

3. **Final Selection**:
    - Chose the top 5 articles from the ranked list to be included in the "See Also" section.


## Contributors

- Kenya Williams
- Mohammad Hijjawi
- Swapnil Bhattacharya
- Richmond Boakye

## Supervisors

- Dr. Huiping Chen
- Dr. Jianqiao Mao


## License

This project is licensed under the MIT License.
