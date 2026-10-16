# Movie Recommendation System

A user-based collaborative filtering project using the MovieLens small ratings dataset.

## Notebook
Open `movie_recommendation_system.ipynb` in Google Colab and run the cells from top to bottom.

## Workflow
1. Load MovieLens movies and ratings.
2. Explore the data and rating patterns.
3. Build a user-based collaborative filtering recommender.
4. Evaluate with a per-user latest-rating holdout split.
5. Save metrics, chart, and report.

## Technologies
- Python
- pandas and NumPy
- scikit-learn
- Matplotlib
- Google Colab

## Results
See `results/evaluation_metrics.csv`, `charts/evaluation_metrics.png`, and `PROJECT_REPORT.md`.

## Dataset
MovieLens latest-small dataset from GroupLens:
https://grouplens.org/datasets/movielens/latest/

The included `ratings.csv` and `movies.csv` are the dataset files used by the notebook.

## Limitations
The evaluation is a single holdout experiment on users with prior ratings. Results are modest and may not generalize to new users or other datasets.
