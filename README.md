# Movie Recommendation System
This project is a Movie Recommendation System built using Python and powered by content-based filtering. The system recommends movies similar to a user-selected movie 
by analyzing key features like genres, cast, crew, and keywords from a dataset of over 4,800 movies.

## Features
- Preprocesses and cleans movie data from the TMDB dataset.
- Extracts important features such as genres, cast, crew, and keywords.
- Combines features into a unified "tags" column for similarity calculation.
- Utilizes Natural Language Processing (NLP) for stemming and cleaning data.
- Computes movie similarity using cosine similarity.
- Recommends top 5 movies based on user input.
## Dataset
- Movies Dataset: tmdb_5000_movies.csv
- Credits Dataset: tmdb_5000_credits.csv
How It Works
## Data Preprocessing:
- Merges movies and credits datasets on the title column.
- Cleans and extracts relevant columns (movie_id, title, overview, genres, keywords, cast, crew).
- Handles missing values and removes duplicates.
## Feature Engineering:
- Converts JSON-like strings in genres, keywords, cast, and crew into lists of keywords.
- Limits the cast list to the top 3 actors and extracts the director from the crew.
- Combines overview, genres, keywords, cast, and crew into a single "tags" column.
## Text Preprocessing:
- Converts tags to lowercase.
- Applies stemming to reduce words to their base forms using the Porter Stemmer.
## Vectorization:
- Converts the tags into numerical vectors using CountVectorizer with a maximum of 5,000 features and removes stopwords.
- Similarity Calculation:
- Calculates the cosine similarity between movie vectors.
## Recommendation:
- Fetches the top 5 movies most similar to the user-selected movie based on cosine similarity scores.

## Clone the repository:
git clone https://github.com/anandreddy05/Movie-Recommendation-System.git

Enter a movie title when prompted.
The system will output the top 5 recommended movies.
Example
Input:
Enter a movie name: Avatar
Output:
# Recommendations:
1. Pirates of the Caribbean: At World's End
2. Spectre
3. The Dark Knight Rises
4. John Carter
5. Guardians of the Galaxy
# Key Libraries Used
- Pandas: For data manipulation and preprocessing.
- NumPy: For numerical operations.
- NLTK: For stemming text data.
- Scikit-learn: For vectorization and similarity calculations
