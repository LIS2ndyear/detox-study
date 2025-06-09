# Digital Detox NLP Analysis

## Overview

Natural Language Processing analysis of Reddit posts comparing digital detox discussions vs. general conversations. Uses computational linguistics to understand emotional and linguistic patterns in digital wellness discourse.

**Main Question**: How does emotional and linguistic framing differ between Reddit posts about digital detox experiences and posts from general, non-detox-related subreddits

## Key Findings

- **Emotional Language**: Detox posts show more struggle and less control
- **Specialized Vocabulary**: Digital wellness communities develop unique terminology
- **Topic Differences**: Clear thematic separation between detox and control groups
- **Authentic Discourse**: Real emotional complexity, not just success stories

## NLP Methods

### Text Analysis Pipeline
1. **Data Collection**: 7,000 Reddit posts via PRAW API
2. **Text Processing**: Cleaning, tokenisation, language detection
3. **Sentiment Analysis**: VAD lexicon (Valence-Arousal-Dominance) + TF-IDF
4. **Topic Modeling**: BERTopic + LDA for theme extraction
5. **Statistical Testing**: Mann-Whitney U tests, Chi-square analysis

## Repository Structure

```
notebooks/
├── 01_data_collection.ipynb          # Reddit scraping with PRAW
├── 02_text_preprocessing.ipynb       # Cleaning and tokenization  
├── 03_topic_modeling.ipynb          # BERTopic clustering
├── 04_sentiment_analysis.ipynb      # VAD + TF-IDF analysis
├── 05_topic_triangulation.ipynb     # LDA vs BERTopic comparison
└── 06_statistical_analysis.ipynb    # Significance testing

data/
├── detox_posts.csv                  # Digital detox Reddit posts
├── control_posts.csv                # General Reddit posts
└── vad_lexicon.txt                  # Emotion norms data
```

## Python Libraries and Packages

- **Data**: `praw`, `pandas`, `langdetect`
- **NLP**: `nltk`, `spacy`, `bertopic`, `sentence-transformers` 
- **ML**: `scikit-learn`, `textblob`
- **Analysis**: `scipy`, `numpy`
- **Viz**: `matplotlib`, `seaborn`, `wordcloud`

## Data Sources

- **Detox Subreddits**: r/digitalminimalism, r/dopaminedetoxing, r/nosurf
- **Control Subreddits**: r/askreddit, r/casualconversation, r/advice
- **Time Range**: 2021-2025
- **Posts**: 3,500 detox + 3,500 control

## Limitations

- Reddit-specific language patterns
- English posts only
- Self-selected digital wellness communities
- Cross-sectional analysis
