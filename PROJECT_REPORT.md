# Movie Recommendation System — Project Report

## Objective
Build and evaluate a user-based collaborative filtering recommender using the MovieLens small ratings dataset.

## Method
The evaluation holds out each user's latest recorded rating. The recommender is built using the remaining ratings only. User similarities are calculated from mean-centered ratings. Movies already rated by a user are excluded from that user's recommendations.

A held-out movie rated 4 or higher is treated as relevant. We report Hit Rate, Precision, Recall, and NDCG at 5 and 10 recommendations.

## Results

| Top-k | Evaluated users | Hit Rate | Precision | Recall | NDCG |
|---:|---:|---:|---:|---:|---:|
| 5 | 363 | 0.0331 | 0.0066 | 0.0331 | 0.0203 |
| 10 | 363 | 0.0689 | 0.0069 | 0.0689 | 0.0314 |

## Interpretation
The model's hit rate is higher at 10 recommendations than at 5, as expected when users receive a longer list. The measured hit rates are modest, so these results should be presented as a baseline experiment rather than evidence of a production-ready recommender.

## Limitations
- This is a single holdout evaluation, not repeated cross-validation.
- It tests users with prior ratings and does not measure recommendations for entirely new users.
- MovieLens is a small public dataset; results may not generalize to other users or catalogs.
- The evaluation uses each user's latest rating as the held-out item and treats ratings of 4 or higher as relevant.
