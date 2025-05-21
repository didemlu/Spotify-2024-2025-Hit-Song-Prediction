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

  
  ## 🔮 Prediction Output

The model outputs a *probability* of being a hit.  
If the probability is over *50%, it's classified as a **potential hit*.

---

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
