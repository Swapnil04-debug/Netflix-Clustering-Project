# 🎬 Netflix Clustering Project

This project explores and clusters Netflix content using unsupervised machine learning techniques. It leverages natural language processing and clustering algorithms to understand patterns, trends, and similarities in TV shows and movies available on Netflix as of 2019.

## 📂 Dataset Overview

The dataset, sourced from [Fixable](https://www.fixable.com/), a third-party Netflix search engine, contains metadata on TV shows and movies available on Netflix. As of the dataset snapshot in 2019:

- **5377 Movies** (≈69.14%)
- **2400 TV Shows** (≈30.86%)

The data includes fields like title, description, cast, director, rating, duration, genres, release year, and country.

## 📊 Key Insights

- **TV vs Movies**: The number of TV shows has tripled since 2010, while the number of movies has dropped by over 2,000.
- **Top Contributors**:
  - *Raul Campos* and *Jan Sulter* have the most listed content.
  - *Anupam Kher* has 38 appearances, followed by *Takahiro Sakurai* and *Shah Rukh Khan*.
- **Country-wise Listings**:
  - 🇺🇸 USA: 2080 Movies, 975 TV Shows
  - 🇮🇳 India: 852 Movies, 71 TV Shows
- **Seasonality**:
  - Major releases in October (785), November (738), December (833), and January (757), indicating a holiday content boost.
- **Ratings**: TV-MA (Mature) is the most common rating for both TV shows and movies.
- **Durations**:
  - Season 1 is the most common TV Show duration.
  - Most movies are between 90–120 minutes.
- **Genres**:
  - Movies: Documentaries > Comedy
  - TV Shows: Drama > International Shows
- **Text Analysis**:
  - Common words in titles: *love*, *Christmas*, *world*, *man*, *life*
  - Common words in descriptions: *family*, *new*, *love*, *life*, *mother*, *find*

## 🧹 Data Preprocessing

- **Used Columns**: `description`, `listed_in`, `rating`, `country`, `title`, `director`, `cast`
- **Steps**:
  - Text converted to lowercase
  - Stopwords removed
  - Stemming applied
  - Vectorized using **TF-IDF (Term Frequency-Inverse Document Frequency)**
  - Dimensionality reduction using **PCA** with 3000 components

## 🤖 Modeling Techniques

We applied multiple clustering methods to discover hidden patterns in the content:

- **KMeans Clustering**
  - Elbow Method used to determine optimal `k`
- **Agglomerative Clustering**
  - Dendrograms used for visualizing cluster hierarchy
- **Silhouette Score** used to evaluate clustering performance

## 🎨 Visualization

- **Word Clouds** were generated for each cluster to highlight dominant themes and keywords.
- Various plots (e.g., release trends, top actors/directors, durations) help in visualizing insights from the data.

## 🔍 Future Enhancements

- Integrate with **IMDb** and **Rotten Tomatoes** ratings for deeper insight.
- Use **deep learning** for more advanced text embedding (e.g., BERT).
- Build a **movie recommendation system** based on cluster similarity.

## 📁 Project Structure
netflix-clustering-project/
│
├── Netflix_Clustering.ipynb     # Main Jupyter Notebook containing the entire analysis and clustering code
├── README.md                    # Project overview, summary, and documentation



## 🛠 Tech Stack

- Python 🐍
- Pandas & NumPy
- Scikit-learn
- Matplotlib & Seaborn
- NLTK
- TF-IDF & PCA
- KMeans & Agglomerative Clustering

## 🙌 Acknowledgments

- Netflix dataset from [Kaggle](https://www.kaggle.com/shivamb/netflix-shows)
- Fixable for Netflix content metadata

---

