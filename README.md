# 🎬 Movie Recommender System
A content-based movie recommender system built with Python and Streamlit. This application suggests movies similar to a user's choice based on a variety of features, including genre, keywords, cast, and crew. The recommendation engine uses a cosine similarity model built on the TMDB 5000 Movie Dataset.

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

