# 🎬 Movie Recommender System
A content-based movie recommender system built with Python and Streamlit. This application suggests movies similar to a user's choice based on a variety of features, including genre, keywords, cast, and crew. The recommendation engine uses a cosine similarity model built on the TMDB 5000 Movie Dataset.


## 🚀 Model Working

<img width="2166" height="1302" alt="Model workflow - visual selection" src="https://github.com/user-attachments/assets/5f43a370-74bb-44fb-a4af-21b73c91c742" />


### Bag of Words
The "Bag of Words" (BoW) model is a simplifying representation used in natural language processing and information retrieval. In this notebook, the BoW model is implemented using CountVectorizer from the scikit-learn library. It works by creating a vocabulary of all unique words from the movie's textual features (like the overview, genres, keywords, cast, and crew). Each movie is then represented as a vector, where each element in the vector corresponds to a word in the vocabulary, and its value is the number of times that word appears in the movie's text. The order of the words is disregarded, hence the term "bag of words."

### Vectorization
Vectorization is the process of converting text into a numerical format that a machine learning model can understand. In this notebook, the CountVectorizer is used to perform vectorization. After creating a combined string of text for each movie that includes its overview, genres, keywords, and information about the cast and crew, the CountVectorizer transforms this text into a matrix. Each row of the matrix corresponds to a movie, and each column corresponds to a unique word in the entire corpus of movie descriptions. The values in the matrix are the counts of each word in each movie's combined text.

### Cosine Similarity
After vectorizing the text data, the notebook uses cosine similarity to measure the similarity between movies. Cosine similarity is a metric used to determine how similar two vectors are, irrespective of their size. It calculates the cosine of the angle between two vectors. A cosine value of 1 means the two vectors are identical, 0 means they are unrelated, and -1 means they are opposites. In this context, the closer the cosine similarity score is to 1, the more similar the movies are in terms of their content. The recommender system uses this similarity score to find the movies that are most similar to a given movie and then suggests them as recommendations.


## 🚀 Features


🧠 Content-Based Filtering: Recommends movies by analyzing shared attributes like genre, cast, director, and plot keywords.

🌐 Interactive Web UI: A clean and simple user interface built with Streamlit that allows users to select a movie and instantly get recommendations.

🖼️ Dynamic Poster Fetching: Fetches and displays movie posters in real-time using the TMDB API for a richer user experience.

⚡ Fast & Efficient: Pre-computes the similarity matrix, allowing for near-instantaneous recommendations once the app is running.

## 🛠 Tech Stack

👨‍💻 Backend & Core Logic
<br>
Python 3.x

Streamlit – For creating and deploying the interactive web application.

🧠 Data Processing & Modeling
<br>
Pandas – For data manipulation and processing of the movie dataset.

NumPy – For numerical operations.

Scikit-learn – Used for calculating the cosine similarity matrix after text vectorization.

Jupyter Notebook – For the exploratory data analysis, data preprocessing, and model building workflow.

📦 API Integrations
<br>
TMDB API – Used to fetch movie details and poster images.

📁 Data Source
<br>
TMDB 5000 Movie Dataset – A static dataset from Kaggle containing metadata for ~5000 movies.

🌐 Frontend
<br>
HTML/CSS (via Streamlit) – Streamlit handles the frontend rendering, allowing for rapid UI development in Python.

## 📸 Demo Screenshots

<img width="1918" height="985" alt="image" src="https://github.com/user-attachments/assets/902a9771-0cd9-45c0-a18b-657a7ba3b251" />
<img width="1918" height="983" alt="image" src="https://github.com/user-attachments/assets/0b95a19e-70a8-4510-842e-6d776026d378" />
<img width="1917" height="987" alt="image" src="https://github.com/user-attachments/assets/381ca8c7-1d12-4f4f-9cb3-66d3973a1356" />



## Getting Recommendations
⚙️ Setup and Installation
1. Clone the Repository
git clone [https://github.com/your-username/movie-recommender-system.git]([https://github.com/your-username/movie-recommender-system.git](https://github.com/AaryaButolia11/Movie-Recommendation-System))
cd movie-recommender-system

2. Get a TMDB API Key
The application requires an API key from The Movie Database (TMDB) to fetch movie posters.

Create a free account on themoviedb.org.

Go to your account Settings → API and copy your API Key.

Open the app.py file and paste your key into the fetch_poster function, replacing the placeholder key.

## In app.py
def fetch_poster(movie_id):
    url = "[https://api.themoviedb.org/3/movie/](https://api.themoviedb.org/3/movie/){}?api_key=YOUR_API_KEY_HERE&language=en-US".format(movie_id)
    # ... rest of the function

3. Install Dependencies
It is recommended to create a virtual environment first.

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt

4. Generate the Model Files
Run the movie_recommender.ipynb notebook. This notebook contains all the data preprocessing and model-building steps. Running it will generate two essential files:

movie_list.pkl: A serialized list of movie data.

similarity.pkl: The pre-computed cosine similarity matrix.

5. Run the Streamlit App
Once the .pkl files are in your project directory, run the following command in your terminal:

streamlit run app.py

The application will open in your default web browser at http://localhost:8501.

## 📁 File Structure
<img width="916" height="295" alt="image" src="https://github.com/user-attachments/assets/f5f7b4b5-de9d-4a3f-af90-487888d70a65" />

