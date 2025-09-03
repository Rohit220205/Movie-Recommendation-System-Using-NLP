# Movie-Recommendation-System-Using-NLP

## Objective:
The goal of this project was to analyze movie plots from IMDb and Wikipedia to determine the similarity between movies and group them into clusters based on their content. The project combined natural language processing (NLP) and unsupervised machine learning techniques to quantify similarity and visualize relationships between movies.

## Steps and Methodology

### Data Import and Observation:

Loaded a dataset of 100 movies containing information like title, genre, Wikipedia plot, and IMDb plot.

Observed that each movie often had two plot summaries written in different styles and tones.

### Combining Plot Summaries:

Merged Wikipedia and IMDb plot summaries into a single column to create a unified text representation.

Prepended the genre to the plot summaries so that genre-specific context was included in similarity calculations.

### Text Preprocessing:

Tokenization: Broke down plots into individual words using NLTK, filtering out numbers and punctuation.

Stemming: Reduced words to their root forms using the Snowball Stemmer (e.g., "witnesses" → "wit"), improving the model's ability to recognize similar words.

Combined tokenization and stemming into a reusable function for efficient processing.

### Vectorization (TF-IDF):

Converted textual plots into numerical vectors using TF-IDF (Term Frequency–Inverse Document Frequency), which emphasizes words that are important and unique to each plot.

Configured to handle unigrams, bigrams, and trigrams, with stopwords removal.

### Clustering Using K-Means:

Applied K-Means clustering to group movies into 5 clusters based on plot similarities.

Each cluster represented movies with similar thematic content (e.g., Drama, Adventure, Biography).

### Similarity Calculation:

Calculated cosine similarity between the TF-IDF vectors of all movies to quantify how similar two movies are based on their plots.

Converted similarity into a distance metric (1 - cosine similarity) for hierarchical clustering.

### Hierarchical Clustering & Dendrogram:

Performed hierarchical clustering and plotted a dendrogram to visualize relationships between movies.

The dendrogram showed which movies were most similar to each other at different levels of similarity.

### Finding Most Similar Movies:

Example: Determined the movies most similar to Braveheart by analyzing similarity scores.

Top 5 similar movies included Star Wars, Vertigo, 2001: A Space Odyssey, The Exorcist, and Psycho.

## Key Outcomes

Successfully preprocessed and unified plot data from multiple sources.

Implemented TF-IDF vectorization and text-based similarity measures to quantify relationships between movies.

Applied unsupervised learning (K-Means and hierarchical clustering) to group movies and visualize their similarity.

Identified the top movies similar to a given title, demonstrating practical applications for recommendation systems.

## Skills and Tools Used

Programming Languages & Libraries: Python, Pandas, NumPy, NLTK, Scikit-learn, Matplotlib, SciPy

NLP Techniques: Tokenization, Stemming, TF-IDF vectorization

Machine Learning: K-Means clustering, Hierarchical clustering

Visualization: Dendrograms, similarity plots

## Impact / Application

This project mimics the logic behind movie recommendation systems, helping platforms like Netflix or IMDb suggest movies to users based on plot similarities. The dendrogram also provides a visual insight into how movies are related by genre, theme, or plot content.
