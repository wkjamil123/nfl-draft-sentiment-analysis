# NFL Draft Sentiment Analysis

## Overview
This project applies natural language processing (NLP) techniques to NFL prospect scouting reports to analyze how evaluative language relates to draft outcomes.

By combining prospect writeups with actual draft results, the analysis explores whether sentiment in scouting language aligns with player grades, draft position, and positional trends across multiple draft classes.

---

## Dataset

This project uses two primary datasets:

- `nfl_prospects_writeup.csv`  
  Contains prospect bios, player grades, positions, and draft class  

- `all_decade_draft.csv`  
  Contains official draft outcomes including round, pick number, and position  

The datasets are merged to connect pre-draft language with actual draft outcomes.

---

## Approach

The analysis follows these steps:

1. **Text Preprocessing**
   - Lowercasing, punctuation removal, and tokenization  
   - Stopword removal and normalization  
   - Creation of cleaned text fields for analysis  

2. **Sentiment Analysis**
   - Sentiment scores computed using TextBlob polarity  
   - Each prospect assigned a sentiment score based on scouting writeups  

3. **Feature Engineering**
   - Bio length calculated as a proxy for evaluation detail  
   - Player grades standardized and categorized into expected success tiers  

4. **Data Integration**
   - Prospect data merged with draft results  
   - Enables comparison between sentiment and actual draft outcomes  

---

## Key Questions

- Does sentiment in scouting reports correlate with draft position?  
- How does sentiment vary across positions and draft classes?  
- Do more detailed scouting reports (longer bios) align with higher-rated players?  
- Are certain positions described more positively than others?  

---

## Key Findings

- Sentiment shows a **relationship with draft position**, with more positive writeups generally associated with earlier selections  
- Player grades and sentiment are positively aligned, suggesting consistency in evaluation language  
- Certain position groups exhibit distinct sentiment patterns across draft classes  
- Bio length varies across prospects and may reflect evaluation depth  

---

## Visualizations

The project includes multiple visual analyses:

- Sentiment vs Player Grade scatter plots  
- Sentiment vs Draft Pick relationships  
- Distribution of grades by expected success categories  
- Positional sentiment trends over time  
- Heatmaps of sentiment by position and draft class  
- Word cloud of common scouting language  

---

## Repository Structure

```
nfl-draft-sentiment-analysis/
│
├── notebooks/
│   ├── NFL Sentiment Analysis.ipynb
│   └── NFL Sentiment Analysis - Original Notebook.ipynb
│
├── data/
│   ├── nfl_prospects_writeup.csv
│   └── all_decade_draft.csv
│
└── README.md
```

---

## How to Run

1. Install required libraries:
   - pandas  
   - numpy  
   - matplotlib  
   - seaborn  
   - nltk  
   - textblob  
   - wordcloud  

2. Download NLTK resources:
```python
import nltk
nltk.download("stopwords")
nltk.download("punkt")
```

3. Run the notebook:
```
notebooks/NFL Sentiment Analysis.ipynb
```

---

## Key Takeaways

- Demonstrates application of NLP techniques to real-world text data  
- Shows how sentiment analysis can be integrated with structured data  
- Highlights relationships between language, evaluation metrics, and outcomes  
- Provides insight into how scouting narratives reflect player value  

---

## Author

Waleed Jamil  
Syracuse University – Applied Data Science
