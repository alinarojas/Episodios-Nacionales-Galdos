# Analysis of the *Episodios Nacionales*: First Series by Galdós

This project analyzes the first series of the *Episodios Nacionales* by Benito Pérez Galdós, which recounts key events in Spanish history between 1805 and 1812, blending fiction with historical facts. By employing advanced text mining and social network analysis (SNA) techniques, the study explores recurring themes, word usage patterns, stylistic evolution, and character interactions. This approach provides a comprehensive understanding of the novels and their critical portrayal of 19th-century Spanish society.

## Data Source

- **Texts from:** Project Gutenberg
- **Novels Analyzed:**
  - *Trafalgar* (1873)
  - *La corte de Carlos IV* (1873)
  - *El 19 de marzo y el 2 de mayo* (1873)
  - *Bailén* (1873)
  - *Napoleón en Chamartín* (1874)
  - *Zaragoza* (1874)
  - *Gerona* (1874)
  - *Cádiz* (1874)
  - *Juan Martín el Empecinado* (1874)
  - *La batalla de los Arapiles* (1875)


## Project Overview

The purpose of this project is to utilize both quantitative and qualitative methods to extract deeper insights from Galdós's work:

### Text Mining
Advanced techniques are used to explore themes, word frequency, and stylistic evolution across the novels. This includes:

- **Word Frequency Analysis:** Creating word clouds to visualize the most common words and identify prevalent themes.
- **Line Graphs:** Plotting the number of lines per chapter to analyze structural patterns.
- **TF-IDF Analysis:** Assessing the importance of key words in each novel relative to the entire series.
- **Zipf's Law Examination:** Analyzing word frequency distributions to understand linguistic patterns.
- **Topic Modeling:** Utilizing **BERTopic**, an advanced topic modeling technique based on BERT, to identify and extract main topics. Traditional methods, like LDA and LSA, were initially attempted but proved less effective due to the predominance of proper nouns in the texts. BERTopic overcomes these limitations by generating high-quality embeddings and incorporating TF-IDF to create more relevant and contextual term representations.
- **Sentiment Analysis:** Evaluating the emotions and sentiments expressed in the texts to gain insight into narrative tone and character perspectives (performed using the **syuzhet** library in R).


### Social Network Analysis (SNA)

Constructing a social network of characters to analyze relationships and interactions. This includes:

- **Character Extraction:**

  - **Standard NLP Techniques:** Using **spaCy** and **NLTK** for tokenization and named entity recognition to identify characters in the texts.
  
  - **Advanced NLP Models:** Implemented a BERT-based NER pipeline using **Transformers** from Hugging Face to improve character name extraction. This enhanced method increases accuracy by leveraging deep language understanding.

- **Interaction Mapping:** Generating combinations of characters appearing together to map their interactions throughout the novels.


## Technologies and Tools Used

- **Text Mining and Sentiment Analysis:**
  - **Python:** Pandas, NLTK, spaCy, BERTopic
  - **R:** Quanteda, TidyText, syuzhet

- **Social Network Analysis (SNA):**
  - **Data Processing and Extraction:** Pandas, NLTK, spaCy, Transformers (Python)
  - **Network Visualization:** igraph (R), Gephi (External visualization tool)
