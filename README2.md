# 🎵 Spotify Hit Song Predictor

A logistic regression-based model to predict hit songs on Spotify  
  Akbank & Machine Learning Bootcamp (2024–2025) Project

---

##  Objective

Use audio-based characteristics like tempo, danceability, loudness, etc. to determine whether a song is likely to be a **hit** on Spotify.

---

##  Dataset

The dataset includes global top Spotify songs of 2024:

- **Source**: Provided on Kaggle  
- **Columns include**:
  - `tempo`
  - `danceability`
  - `popularity`
  - `loudness`
  - `speechiness`
  - `acousticness`
  - `valence`
  - `liveness`
  - `daily_movement`
  - *(Optional)* `artist_popularity` (via Spotify API)

---

##  Methods Used

- Exploratory Data Analysis (EDA)  
- Data Preprocessing  
- Logistic Regression (Binary Classification)  
- Accuracy & Probability-based Evaluation  
- Visualizations (Seaborn & Matplotlib)  
- *(Optional)* Spotify API integration with `spotipy`

---

##  Features Used

- `tempo`  
- `danceability`  
- `loudness`  
- `speechiness`  
- `acousticness`  
- `valence`  
- `liveness`  
- `daily_movement`  
- `popularity` *(used for label definition)*

---

##  Prediction Output

The model outputs a **probability** of being a hit.  
If the probability is over **50%**, it's classified as a **potential hit**.

---

##  How to Run the Project

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/spotify-hit-prediction.git
cd spotify-hit-prediction
pip install -r requirements.txt
jupyter notebook
# or
python main.py

```python
...
```
## 💻 User Input Mode

To obtain immediate predictions, users can manually enter values via the command line:

```python
Please enter the following music features:
Tempo (e.g., 120.0): 118
Danceability (0-1): 0.75
Loudness (e.g., -5.0): -4.2
...
🎯 Prediction: ✅ Might Be a Hit!

```python
...
```
🔧 Improving the Project
This project can be enhanced in several meaningful ways. Here are ideas for future development:

1️⃣ Use More Sophisticated Models
Replace logistic regression with advanced models such as:

Random Forest

Gradient Boosting

Neural Networks

📌 Example (Random Forest):



