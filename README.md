# 🎥 Movie Recommendation Chatbot

This is a chatbot that provides movie recommendations based on user input, such as a **genre** (e.g., Action, Comedy) or an **actor's name** (e.g., Leonardo DiCaprio). The chatbot leverages the **OMDb API**, **NLP techniques**, and **FastAPI** to deliver personalized movie suggestions.  
We are also working on integrating **Wikipedia** to enhance the information provided about movies, genres, and actors.

---

## 🚀 Features

- Accepts queries like:
  - "Recommend some action movies."
  - "Show me movies starring Leonardo DiCaprio."
- Fetches movie data (title, plot, genre, rating, etc.) from the OMDb API.
- Uses **NLP** to extract entities (genre, actor) from user input.
- Provides up to **5 or 10 movie recommendations** per query.
- Built with **FastAPI** for fast, asynchronous performance.
- **Upcoming Feature**: Wikipedia integration for detailed information about movies, genres, and actors.

---

## 🛠️ Tech Stack

- **Python**: Core programming language.
- **FastAPI**: Framework for building the chatbot backend.
- **spaCy**: For natural language processing (NLP).
- **FuzzyWuzzy**: For fuzzy matching of actor names.
- **OMDb API**: For fetching movie data.
- **Uvicorn**: ASGI server to run the FastAPI application.
- **Wikipedia API** (In Progress): To fetch additional details about movies and related topics.

---

## 📂 Project Structure

```plaintext
movie-recommendation-chatbot/
├── app.py               # Main application file
├── static/              # Static assets for UI (e.g., index.html)
│   └── index.html
├── movie_utils.py       # Movie recommendation logic
├── nlp_utils.py         # NLP-related logic for user queries
├── requirements.txt     # Dependencies
├── README.md            # Project overview
└── config.py            # (Excluded in GitHub) Contains API keys
```

---

## ⚙️ Prerequisites

1. **Python 3.9 or higher**: Ensure Python is installed.
2. **OMDb API Key**: Get an API key from [OMDb API](http://www.omdbapi.com/). - Get Your Key With In Hour !!!!!

---

## 🔧 Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/R-Mahesh45/movie-recommendation-chatbot.git
   cd movie-recommendation-chatbot
   ```

2. **Install Dependencies**:
   Use the `requirements.txt` file to install dependencies.
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up API Keys**:
   Create a `config.py` file in the project root and add:
   ```python
   OMDB_API_KEY = "your_api_key_here" - i have removed mine 
   OMDB_API_URL = "http://www.omdbapi.com/"
   ```

4. **Run the Application**:
   Start the FastAPI application using Uvicorn.
   ```bash
   uvicorn app:app --reload
   ```
   The app will run at: [http://127.0.0.1:8000](http://127.0.0.1:8000)

---

## 🖥️ How to Use

1. Open your browser and navigate to [http://127.0.0.1:8000/static/index.html](http://127.0.0.1:8000/static/index.html).
2. Enter your query, such as:
   - "Show me some action movies."
   - "What are the top 5 Leonardo DiCaprio movies?"
3. The chatbot will respond with movie recommendations.

---

## ✨ Example Output

**User Input**: "Recommend some action movies."  
**Bot Output**:
```
Here are the top action movies:
1. The Dark Knight (2008)
   - Genre: Action, Crime, Drama
   - IMDb Rating: 9.0
   - Plot: When the menace known as The Joker wreaks havoc...
   - Starring: Christian Bale, Heath Ledger

2. Inception (2010)
   - Genre: Action, Adventure, Sci-Fi
   - IMDb Rating: 8.8
   - Plot: A thief who steals corporate secrets...
   - Starring: Leonardo DiCaprio, Joseph Gordon-Levitt
```

---

## 🛠️ Key Functions

### 1. **Movie Recommendation (`movie_utils.py`)**
Fetches movies from the OMDb API and provides detailed information, including:
- Title, genre, plot, actors, rating, and poster.

### 2. **Natural Language Processing (`nlp_utils.py`)**
- Extracts genres and actors using **spaCy**.
- Fuzzy matches actor names using **FuzzyWuzzy**.

---

## 🚀 Future Enhancements

- Add support for director-based queries.
- Improve recommendations using collaborative filtering or content-based algorithms.
- Deploy the chatbot to a live server (e.g., AWS, Heroku).
- Enhance the UI for better user experience.
- **Wikipedia Integration**: Fetch in-depth information about movies, genres, and actors directly from Wikipedia.

---

## 🖋️ License

This project is licensed under the MIT License. Feel free to use and modify it!

---

## 💬 Feedback

If you have suggestions or feedback, feel free to open an issue or contribute to the project. Your input is appreciated!
