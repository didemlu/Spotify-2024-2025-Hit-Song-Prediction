#   Spotify-hit-song-predictor
A logistic regression-based model to predict hit songs on Spotify (Akbank ML Bootcamp Project)

This project uses machine learning techniques to predict whether a song will become a **hit** or **non-hit** based on its audio features created for the 2024–2025 Akbank & Machine Learning Bootcamp.


---

## Objective

Use audio-based characteristics like tempo, danceability, loudness, etc. to determine whether a song is likely to be a **hit** on Spotify.
---

## 📁 Dataset

The dataset includes global top Spotify songs of 2024:

- Source: Provided on Kaggle
- Columns include:
  - `tempo`
  - `danceability`
  - `popularity`
  - `loudness`
  - `speechiness`
  - `acousticness`
  - `valence`
  - `liveness`
  - `daily_movement`
  - (Optional: `artist_popularity`, when available via API)

---

## Methods Used

- Exploratory Data Analysis (EDA)
- Data Preprocessing
- Logistic Regression (Binary Classification)
- Accuracy & Probability-based Evaluation
- Visualizations with Seaborn & Matplotlib
- (Optional) Spotify API integration with `spotipy`

---

## Features Used

- `tempo`
- `danceability`
- `loudness`
- `speechiness`
- `acousticness`
- `valence`
- `liveness`
- `daily_movement`
- `popularity` (used for label definition)

  
  ## Prediction Output

The model outputs a *probability* of being a hit.  
If the probability is over *50%, it's classified as a **potential hit*.

---

## 🚀 How to Run the Project

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/spotify-hit-prediction.git
cd spotify-hit-prediction
pip install -r requirements.txt
jupyter notebook
# or
python main.py

## 💻 User Input Mode

To obtain immediate predictions, users can manually enter values for each feature using the command line.

For instance:

```python
 Please enter the following music features:
Tempo (e.g., 120.0): 118
Danceability (0-1): 0.75
Loudness (e.g., -5.0): -4.2
...
🎯 Prediction: ✅ Might Be a Hit!

## 🔧 Improving the Project

This project can be enhanced in several meaningful ways. Here are ideas for future development and how to implement them:

---

### 1. Use More Sophisticated Models

Replace logistic regression with advanced models such as:

* **Random Forest**
* **Gradient Boosting**
* **Neural Networks (Deep Learning)**

📌 Example (Random Forest):

```python
from sklearn.ensemble import RandomForestClassifier

model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(x_train, y_train)
```

---

### 2. Expand the Dataset

* Add more years of Spotify data (e.g., 2019–2023).
* Include different genres or regions.
* Combine multiple CSVs using `pandas.concat()` to enrich data variety.

---

### 3. Automate Spotify API Integration

Allow users to paste a **Spotify track URL** and automatically:

* Extract audio features
* Retrieve artist popularity

✅ Already partially implemented with `spotipy`, but could be made more robust.

---

### 4. Add External Variables

Consider adding additional contextual features such as:

* **Artist popularity** (already available via Spotify API)
* **GDP per capita** of user's country (can use `worldbank` or public APIs)
* **Country-specific music trends** to improve prediction accuracy

---

### 5. Build a Web Interface

Make the model accessible through a user-friendly UI.

✅ Tools to consider:

* **Streamlit**: Easy and Pythonic
* **Flask** or **Django**: More customizable for full-stack apps

📌 Example:

```bash
streamlit run app.py
```

---

### 6. Accept Audio File Uploads

Let users upload `.mp3` or `.wav` files. Then use audio processing libraries to extract song features:

✅ Libraries:

* [`librosa`](https://librosa.org/)
* [`pydub`](https://github.com/jiaaro/pydub)

📌 Example:

```python
import librosa

y, sr = librosa.load("song.mp3")
tempo, _ = librosa.beat.beat_track(y, sr=sr)
```

---

Feel free to open issues or contribute with pull requests if you want to help expand the project!
