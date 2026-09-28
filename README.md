# DSA 4060 Week 2: Recommendation Data and Popularity Baselines

## Task
Clean and explore a movie ratings dataset, build a user-item matrix, measure its sparsity, and build a popularity-based recommender.

## Files
- `DSA_4060_Week_2_Practical_Task.ipynb`: completed notebook with explanations
- `DSA_4060_Week2_Movie_Ratings.csv`: the dataset
- `top_10_recommended_movies.csv`: the top 10 recommended movies

## Data Cleaning
- Started with 509 records.
- Removed 3 duplicate rows and 3 rows with missing user or movie IDs.
- Removed 3 ratings outside the 1 to 5 scale (-1, 0 and 6), leaving 500 records.
- Found 70 repeated user-movie pairs (users who rated the same movie again later) and kept only the latest rating per pair, leaving 430 ratings.

## Findings
- 430 ratings from 50 users on 24 movies; average rating 3.48.
- Most active user: U016 (12 ratings). Most-rated movie: Nairobi Nights (27 ratings).
- Sparsity: 64.17% (430 of 1,200 possible ratings observed).
- Top 10 movies with at least 10 ratings, ranked by average rating:

| Rank | Movie | Average Rating | Ratings |
|------|-------|---------------|---------|
| 1 | Market Day | 4.50 | 14 |
| 2 | Midnight in Mombasa | 4.35 | 17 |
| 3 | Code Breakers | 4.21 | 14 |
| 4 | Hidden Lake | 4.14 | 14 |
| 5 | Home Again | 4.13 | 15 |
| 6 | Future Africa | 4.07 | 14 |
| 7 | Mountain Echoes | 4.00 | 26 |
| 8 | City of Tomorrow | 3.93 | 27 |
| 9 | Coastal Dreams | 3.77 | 22 |
| 10 | The Final Goal | 3.75 | 16 |

## Interpretation
The top movies have the highest average ratings among movies with enough ratings to be reliable. Popularity-based recommendation is simple and works for new users, but it is not personalised and it favours movies that already have many ratings.
