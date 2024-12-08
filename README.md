# Movie Recommendation System
Author: Chris Kucewicz

## Business Understanding

### Background

The Kanopy app is a movie streaming service widely used by public libraries and universities, offering a vast library of films, documentaries, educational content, and more. While Kanopy has a dedicated user base, it faces challenges in competing with larger, more popular streaming platforms like Netflix and Hulu. One key factor contributing to this challenge is that Kanopy does not currently ask or require users to rate movies. As a result, the platform lacks the kind of personalized content recommendations that are a hallmark of other streaming services. By implementing a collaborative filtering recommendation system that leverages user ratings and the ratings of similar users, Kanopy can provide more tailored movie suggestions. This approach will help users discover new content, boost engagement, and increase user retention. 

### Business Goals
The primary goal of this project is to develop and implement a personalized movie recommendation system model for the Kanopy app. Using collaborative filtering techniques, the system will provide users with top 5 movie recommendations based on the ratings of similar users and the user’s own past ratings and viewing history.

### Business Success Criteria
The success of this project will be evaluated based on the accuracy and relevance of the movie recommendations generated by the system. Specifically, the system will aim to provide each user with a list of their top 5 recommended movies tailored to their preferences.

To measure the effectiveness of the recommendations, the project will use Root Mean Square Error (RMSE) as the primary evaluation metric. RMSE quantifies the difference between the predicted ratings and the actual user ratings for movies. A lower RMSE indicates better predictive accuracy, meaning the recommendations align more closely with user preferences.

Achieving a competitive RMSE score will demonstrate that the recommendation system is capable of delivering meaningful and personalized suggestions. This, in turn, is expected to enhance user satisfaction, increase engagement with the platform, and boost user retention—key factors in Kanopy’s ability to compete in the crowded streaming market.

## Data Understanding
This project used data from MovieLens’ database, specifically focusing on two datasets: `movies.csv` and `ratings.csv`.

`movies.csv`: This dataset contains over 9,000 observations, with each row representing a unique movie identified by a movieId. Additional information about each movie includes its title (which includes the year of release in parentheses) and its associated genres (Action, Comedy, Drama, etc.)

`ratings.csv`: This dataset provides detailed information on user ratings, with over 100,000 observations. Each row represents a single rating provided by a user for a specific movie. Key fields include userId (an identifier for the user), movieId (linking the rating to a movie in the `movies.csv` dataset), rating (0-5 stars with 0.5 increments), and timestamp (indicating when the rating was made).

### Data Preparation
The `movies` and `ratings` dataframes were well-structured, requiring minimal data preparation. There were no issues with null values, incorrect datatypes, or the need to rename features, so the data preparation phase was relatively short. The main steps involved merging the two datasets using an inner join, which helped facilitate a more comprehensive Exploratory Data Analysis (EDA) by combining relevant information from both. Additionally, the `timestamp` feature was removed from the merged dataset, as it does not contribute to the functionality of the recommender system or the EDA.
Lastly, I dropped `timestamp` from `ratings` so `ratings` was prepared for use in the Surprise models. 

## Exploratory Data Analysis
Key findings:
* There is a ***weak, positive*** correlation (**0.1273**) between a movie’s number of ratings and overall rating, indicating that popular movies tend to receive slightly higher ratings.
* The three most popular movies by number of reviews are *Forrest Gump*, *Shawshank Redemption*, and *Pulp Fiction*.
* By average rating, the *Film-Noir* genre is the highest rated (**3.92**), while *Horror* movies are the lowest rated (**3.28**).

## Model

## Evaluation

## Conclusion

### Limitations

### Recommendations

### Next Steps

## Additional Information

View the full project in the Jupyter Notebook
Contact Chris Kucewicz at cfkucewicz@gmail.com with additional questions.

## Repository Structure
