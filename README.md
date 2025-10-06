# 🎬 Movie Recommender System

> *"In a world full of movies, find the ones that truly match your vibe."*  
A simple yet effective recommender system that suggests movies based on similarity and content features.

---

## 📌 Overview

This project is a **Content-Based Movie Recommender System** implemented in **Python using Flask**.  
It leverages **similarity algorithms** to provide personalized movie suggestions based on genres, keywords, and descriptions.

---

## 📂 Project Structure

Movie-Recommender-System/
├── app.py # Main Flask application script
├── requirements.txt # Python dependencies
└── README.md # Documentation

yaml
Copy code

---

## ⚙️ Installation

### 1. Clone the repository

git clone https://github.com/khaivutri/Movie-Recommender-System.git
cd Movie-Recommender-System

###2. Set up a virtual environment (recommended)
bash
Copy code
python3 -m venv venv
source venv/bin/activate       # macOS / Linux
# venv\Scripts\activate        # Windows

###3. Install dependencies
bash
Copy code
pip install -r requirements.txt
🚀 Usage
Run the application:

bash
Copy code
python app.py
After starting, open your browser and navigate to:

arduino
Copy code
http://localhost:5000
You can enter a movie name (e.g., "The Dark Knight" or "Pulp Fiction"),
and the system will return a list of recommended movies based on content similarity.

🔎 How It Works
This recommender system is Content-Based, and works as follows:

Data Preparation

A small dataset of movie titles, genres, and descriptions is loaded inside app.py.

In real-world usage, this data would come from a file like movies_dict.pkl.

Feature Vectorization

Textual features (descriptions/tags) are converted into numerical vectors using TF-IDF (Term Frequency-Inverse Document Frequency).

Similarity Calculation

Cosine Similarity is computed between movie vectors.

Smaller angle → higher similarity.

Recommendation

Given an input movie, the system finds its index, retrieves similarity scores,
and returns the Top-10 most similar movies.

✅ Features
🎥 Content-based recommendations

📊 TF-IDF & Cosine Similarity for robust similarity scoring

⚡ Lightweight Flask Web App with instant responses

🖥️ Simple UI for testing movie suggestions

📡 API Endpoints
1. Health Check
GET /
Returns basic status message.

Response:

json
Copy code
{
  "status": "Movie Recommender API is running"
}
2. Get Recommendations
POST /recommend

Request body:

json
Copy code
{
  "movie": "The Dark Knight"
}
Response:

json
Copy code
{
  "input_movie": "The Dark Knight",
  "recommendations": [
    "Batman Begins",
    "Inception",
    "The Prestige",
    "The Dark Knight Rises",
    "Interstellar",
    "Memento",
    "Dunkirk",
    "Joker",
    "V for Vendetta",
    "Watchmen"
  ]
}
📦 Requirements
All dependencies are listed in requirements.txt.
Key libraries include:

Flask

Scikit-learn

Pandas

Numpy

🤝 Contributing
Contributions are welcome! 🎉
Please follow the standard GitHub workflow:

Fork the repository

Create a new branch:

git checkout -b feature/amazing-feature
Commit your changes:

bash
Copy code
git commit -m "Add some amazing feature"
Push to your branch and open a Pull Request.

📜 License
This project is open-source and available under the MIT License.
Feel free to use, modify, and distribute with attribution.

💡 Built with ❤️ for movie lovers everywhere.
