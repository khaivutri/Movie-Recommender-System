# 🎬 Movie Recommender System

> *"In a world full of movies, find the ones that truly match your vibe."*  
> A simple yet effective recommender system that suggests movies based on similarity and content features.

---

## 📌 Overview

This project is a **Content-Based Movie Recommender System** implemented in **Python using Flask**.  
It leverages **similarity algorithms** to provide personalized movie suggestions based on genres, keywords, and descriptions.

---

## 📂 Project Structure

```
Movie-Recommender-System/
├── app.py                # Main Flask application script
├── requirements.txt      # Python dependencies
├── movies_dict.pkl       # Preprocessed movie data (optional)
├── similarity.pkl        # Precomputed similarity matrix (optional)
└── README.md             # Documentation
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/khaivutri/Movie-Recommender-System.git
cd Movie-Recommender-System
```

### 2. Set up a virtual environment (recommended)

```bash
python3 -m venv venv
source venv/bin/activate       # macOS / Linux
# venv\Scripts\activate        # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🚀 Usage

### Run the application:

```bash
python app.py
```

After starting, open your browser and navigate to:

```
http://localhost:5000
```

You can enter a movie name (e.g., "The Dark Knight" or "Pulp Fiction"), and the system will return a list of recommended movies based on content similarity.

---

## 🔎 How It Works

This recommender system is **Content-Based**, and works as follows:

### 1. Data Preparation
A small dataset of movie titles, genres, and descriptions is loaded inside `app.py`.  
In real-world usage, this data would come from a file like `movies_dict.pkl`.

### 2. Feature Vectorization
Textual features (descriptions/tags) are converted into numerical vectors using **TF-IDF** (Term Frequency-Inverse Document Frequency).

### 3. Similarity Calculation
**Cosine Similarity** is computed between movie vectors.  
Smaller angle → higher similarity.

### 4. Recommendation
Given an input movie, the system finds its index, retrieves similarity scores, and returns the **Top-10 most similar movies**.

---

## ✅ Features

- 🎥 **Content-based recommendations**
- 📊 **TF-IDF & Cosine Similarity** for robust similarity scoring
- ⚡ **Lightweight Flask Web App** with instant responses
- 🖥️ **Simple UI** for testing movie suggestions

---

## 📡 API Endpoints

### 1. Health Check

**GET** `/`

Returns basic status message.

**Response:**
```json
{
  "status": "Movie Recommender API is running"
}
```

### 2. Get Recommendations

**POST** `/recommend`

**Request body:**
```json
{
  "movie": "The Dark Knight"
}
```

**Response:**
```json
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
```

---

## 📦 Requirements

All dependencies are listed in `requirements.txt`.

**Key libraries include:**
- Flask
- Scikit-learn
- Pandas
- Numpy

---

## 🤝 Contributing

Contributions are welcome! 🎉

Please follow the standard GitHub workflow:

1. **Fork the repository**
2. **Create a new branch:**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Commit your changes:**
   ```bash
   git commit -m "Add some amazing feature"
   ```
4. **Push to your branch** and open a Pull Request.

---

## 📜 License

This project is open-source and available under the **MIT License**.  
Feel free to use, modify, and distribute with attribution.

---

## 🛠️ Tech Stack

- **Python 3.8+**
- **Flask** - Web framework
- **Scikit-learn** - Machine learning library
- **Pandas** - Data manipulation
- **NumPy** - Numerical computing

---

## 🐛 Troubleshooting

### Port already in use
If port 5000 is occupied, modify `app.py`:
```python
app.run(debug=True, port=5001)
```

### Missing pickle files
If `movies_dict.pkl` or `similarity.pkl` are missing, the app will use sample data or you'll need to generate them from your dataset.

---

## 📧 Contact

For questions or suggestions, feel free to reach out:

- GitHub: [@khaivutri](https://github.com/khaivutri)
- Project Link: [https://github.com/khaivutri/Movie-Recommender-System](https://github.com/khaivutri/Movie-Recommender-System)

---

💡 **Built with ❤️ for movie lovers everywhere.**
