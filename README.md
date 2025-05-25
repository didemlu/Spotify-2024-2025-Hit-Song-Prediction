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
## User Input Mode

To obtain immediate predictions, users can manually enter values via the command line:

```python
Please enter the following music features:
Tempo (e.g., 120.0): 118
Danceability (0-1): 0.75
Loudness (e.g., -5.0): -4.2
...
 Prediction: ✅ Might Be a Hit!

```python
...
```
 Improving the Project
This project can be enhanced in several meaningful ways. Here are ideas for future development:

1- Use More Sophisticated Models
Replace logistic regression with advanced models such as:

Random Forest

Gradient Boosting

Neural Networks

 Example (Random Forest):
```python
from sklearn.ensemble import RandomForestClassifier

model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(x_train, y_train)
```
2- Expand the Dataset
Add more years of Spotify data (e.g., 2019–2023)

Include different genres or regions

Use pandas.concat() to combine multiple CSVs

3- Automate Spotify API Integration
Allow users to paste a Spotify track URL and automatically:

Extract audio features

Retrieve artist popularity

+ Already partially implemented with spotipy

4- Add External Variables
Include context-aware features such as:

Artist popularity (via Spotify API)

GDP per capita (via World Bank/public APIs)

Country-specific music trends

5- Build a Web Interface
Make the model accessible via a web UI.

+ Suggested Tools:

Streamlit – Easy & fast

Flask/Django – Custom & scalable

 Example:
```python
streamlit run app.py
```
6- Accept Audio File Uploads
Allow users to upload .mp3 or .wav files. Extract song features using:

librosa

pydub

 Example:
```python
import librosa

y, sr = librosa.load("song.mp3")
tempo, _ = librosa.beat.beat_track(y, sr=sr)
```
---

##  References

- [Spotify Web API Documentation](https://developer.spotify.com/documentation/web-api/)
- [Kaggle Dataset - Universal Top Spotify Songs 2024](https://www.kaggle.com/)
- [Analytics Vidhya - 10 Best Data Analytics Projects](https://www.analyticsvidhya.com/blog/2023/05/10-best-data-analytics-projects/)
- [Analytics Vidhya - Data Science & Machine Learning Blog](https://www.analyticsvidhya.com/blog/)
- (https://stackoverflow.com/questions)
* Contributing
Feel free to open issues or contribute with pull requests to help expand the project!







