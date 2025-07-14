# Friends TV Show Dialogue Analysis
This project analyzes dialogues from the popular TV show *Friends* using **web scraping**, **text mining**, and **sentiment analysis** techniques.<br> 
The goal is to uncover linguistic patterns and emotional dynamics among the main characters.


## Project Overview
- **Objective**: Extract, clean, and analyze *Friends* scripts to identify dominant emotions, recurring words, and unique character speech styles.
- **Data Source**: HTML episode scripts scraped from a specialized website (*All_Seasons* folder).
- **Data Structure**:
  - Structured table with 3 columns: `Character`, `Dialogue`, and `Episode`.
  - Cleaned and processed using `tidyverse`, `tidytext`, and `rvest`.


## Key Project Features
### 1. Dialogue Extraction
- **Method**: HTML scraping with `rvest` to extract `<p>` elements containing speech.
- **Filtering**: Only lines starting with a character's name (e.g., `Joey:`) are kept.
- **Result**: Over 50,000 cleaned lines of dialogue ready for analysis.

### 2. Word Frequency Analysis
- **Cleaning**: Lowercase conversion, punctuation removal, and stop word filtering.
- **Stemming**: Words reduced to their root forms to group similar terms.
- **Result**: Word clouds per character, visualized using `wordcloud` and `wordcloud2`.

### 3. Sentiment Analysis
- **Lexicons Used**: Bing, NRC, Afinn, Loughran.
- **Sentiment Dimensions**:
  - **Positive vs. Negative** (Bing)
  - **Emotion categories**: trust, fear, anger, joy… (NRC)
  - **Polarity scores** (Afinn)
- **Result**: Visual dashboards showing sentiment trends across dialogues.

### 4. Visualization
- Graphs using `ggplot2` for emotional distribution, polarity scores, and most frequent terms.
- Dynamic and interactive word clouds.
