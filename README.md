# 🎬 Movie Recommendation System

A content-based movie recommendation project built with Python, Pandas, and scikit-learn. It recommends movies based on metadata such as genres, keywords, cast, director, and tagline.

<p align="center">
  <img src="https://img.shields.io/badge/Python-3-%233776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Scikit--Learn-%23F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-Learn" />
  <img src="https://img.shields.io/badge/Pandas-%231504A3?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas" />
  <img src="https://img.shields.io/badge/Jupyter-%23F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter" />
</p>

## Overview

This project uses a movie dataset from Kaggle and builds a recommendation engine by:

- combining textual metadata into a single feature string
- converting text to vectors using TF-IDF
- computing similarity with cosine similarity
- matching the user-entered title to the closest movie name

The dataset source is:

https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata

## Features

- Content-based recommendations
- TF-IDF text vectorization
- Cosine similarity ranking
- Close match title detection using `difflib`
- Jupyter notebook workflow for easy experimentation

## How It Works

1. Load the dataset.
2. Select relevant movie fields such as genres, keywords, tagline, cast, and director.
3. Fill missing values with empty strings.
4. Combine the text fields into one feature per movie.
5. Convert the combined text into numerical vectors with TF-IDF.
6. Compute cosine similarity between all movies.
7. Ask the user for a movie name.
8. Match the entered title to the closest title in the dataset.
9. Recommend movies with the highest similarity scores.

## Project Structure

- `notebooks/Movie_Recommendation_System.ipynb` — main notebook
- `data/movies.csv` — Kaggle dataset file
- `README.md` — project documentation
- `requirements.txt` — Python dependencies
- `.gitignore` — ignores local environment and downloaded dataset files

## Requirements

```bash
pip install -r requirements.txt
```

## Dataset Setup

Download the TMDB dataset from Kaggle:

https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata

Then place the CSV file in the `data/` folder.

Example:

```python
movies_data = pd.read_csv("data/movies.csv")
```

If your downloaded file has a different name, rename it to `movies.csv` or update the path in the notebook.

## Running the Project

1. Open the project folder in Jupyter:

```bash
jupyter notebook
```

2. Open the notebook from `notebooks/Movie_Recommendation_System.ipynb`.

3. Run all cells.

4. Enter a movie name when prompted.

Example:

```text
Enter your favourite movie name: Inception
```

## Example Output

```text
movies suggested for you:

1. The Dark Knight
2. Interstellar
3. Memento
4. Dunkirk
5. Batman Begins
```

## Notes

- This is a content-based recommendation system, not collaborative filtering.
- The quality of recommendations depends on the metadata quality in the dataset.
- The notebook is intended for learning and demonstration purposes.

## License

This project is for educational and demonstration purposes.
