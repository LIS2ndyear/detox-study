# Emotional and Linguistic Framing of Digital Detox

## Overview
Natural Language Processing analysis of Reddit posts comparing digital detox discussions vs. general conversations. Uses computational linguistics and psychometric emotion analysis to understand emotional and thematic patterns in digital wellness discourse.

**Research Questions**: 
- **RQ1**: How do emotional patterns measured through Valence-Arousal-Dominance (VAD) dimensions differ between digital detox and general Reddit community discourse?
- **RQ2**: What thematic content patterns, identified through computational topic modelling, distinguish digital detox communities from general Reddit discourse?

## Key Findings
- **Emotional Profiles**: Detox posts show significantly higher valence (positivity), lower arousal (calmness), and higher dominance (sense of control) compared to general Reddit discourse
- **Thematic Separation**: Digital detox communities focus on social media awareness, systematic detox processes, and personal reflection vs. general life discussions
- **Statistical Significance**: All VAD dimensions show extremely significant differences (p < 10⁻³⁹) with large effect sizes
- **Topic Validation**: Dual modeling approach (BERTopic + LDA) confirms distinct thematic spaces between communities

## NLP Methods

### Text Analysis Pipeline
1. **Data Collection**: 7,000 balanced Reddit posts via PRAW API
2. **Text Processing**: Language detection, tokenisation, quality filtering
3. **Emotional Analysis**: Novel VAD-weighted TF-IDF + TextBlob sentiment validation
4. **Topic Modeling**: BERTopic with sentence transformers + LDA triangulation
5. **Statistical Testing**: Mann-Whitney U tests, Chi-square analysis, Spearman correlations

## Repository Structure
notebooks/
├── 01_data_collection.ipynb           # Reddit API data collection
├── 02_preprocessing.ipynb             # Text cleaning and tokenization
├── 03_topic_modelling_bertopic.ipynb  # Semantic topic clustering
├── 04_emotion_sentiment_analysis.ipynb # VAD-weighted TF-IDF analysis
├── 05_triangulation_lda.ipynb         # LDA validation and comparison
├── 06_statistical_tests.ipynb         # Significance testing and correlations
└── 07_visualisation.ipynb             # PCA, heatmaps, and result visualization
data/
├── detox_posts.csv                    # Digital detox Reddit posts
├── control_posts.csv                  # General Reddit posts
└── vad_lexicon.txt                    # NRC VAD emotion norms

## Python Libraries and Packages
- **Data**: `praw`, `pandas`, `langdetect`, `tqdm`
- **NLP**: `nltk`, `bertopic`, `sentence-transformers`, `textblob`
- **ML**: `scikit-learn`, `umap-learn`, `hdbscan`
- **Analysis**: `scipy`, `numpy`, `matplotlib`, `seaborn`
- **Topic Modelling**: `gensim` (LDA), `plotly` (visualisation)

## Data Sources
- **Detox Subreddits**: r/digitalminimalism, r/dopaminedetoxing, r/digitaldetox, r/nophones, r/nosurf, r/mindfulness
- **Control Subreddits**: r/askreddit, r/offmychest, r/casualconversation, r/nostupidquestions, r/todayilearned, r/advice
- **Time Range**: 2021-2025 (post-COVID baseline)
- **Sample**: 3,500 detox + 3,500 control posts (balanced)
- **Emotion Lexicon**: NRC VAD Lexicon v2.1 (14,000+ emotion norms)

## Limitations
- Reddit-specific discourse patterns and user demographics
- English language posts only
- Self-selected digital wellness communities (selection bias)
- Cross-sectional rather than longitudinal analysis
- Potential confounding variables in community membership
