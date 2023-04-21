# Anime-rating-project
Anime Rating Project


### Objective

Streamist is currently focusing on the anime available in their portal and wants to identify the most important factors involved in rating an anime.  As a data scientist at Streamist, you are tasked with analyzing the  portal's anime data and identifying the important factors by building a predictive model to predict the rating of an anime.


### Variables

1. title: title of the anime
2. mediaType: format of publication
3. eps: number of episodes (movies are considered 1 episode)
4. duration: duration of an episode in minutes
5. startYr: the year that airing started
6. finishYr: the year that airing finished
7. description: the synopsis of the plot
8. contentWarn: content warning
9. watched: number of users that completed it
10. watching: number of users that are watching it
11. rating: average user rating
12. votes: number of votes that contribute to the rating
13. studio_primary: studios responsible for creation
14. studios_colab: whether there was a collaboration between studios for anime production
15. genre: genre to which the anime belongs



## Exploratory Data Analysis (EDA) Results

## Boxplot Results
* Anime available as web series or music videos have a lower rating in general
* Anime under the genre of Drama are rated the highest in general, while those under the genre of Comedy and rated the least
* Anime under the genres of Drama and Romance have higher viewership in general
* Anime from the Drama and Romance genres are being watched more in general
* Anime released as movies or TV speicals have the highest duration while music videos have the lowest, which is expected


## Missing values treatment
* We imputed the missing values with median.

## Feature Engineering
* New feature `years_running` was created by taking the difference between `finishYr` and `startYr` columns
* The original columns `finishYr` and `startYr` was dropped.

## Data Preparation
- Our aim is to predict the rating of an anime
- Before building the model, we encoded our categorical features by using `One Hot Encoding`
- By adding dummy variables to our dataset
- We added a constat

## Model Developement
- A linear regression model was developed using statsmodels 

## Result Interpretation
**Adjusted. R-squared**: It reflects the fit of the model.
    - Adjusted R-squared values generally range from 0 to 1, where a higher value generally indicates a better fit, assuming certain conditions are met.
    - In our case, the value for adj. R-squared is **0.722**, which is good.


2. ***const* coefficient**: It is the Y-intercept.
    - It means that if all the predictor variable coefficients are zero, then the expected output (i.e., Y) would be equal to the *const* coefficient.
    - In our case, the value for `const` coefficient is **2.7707**


3. **Coefficient of a predictor variable**: It represents the change in the output Y due to a change in the predictor variable (everything else held constant).
    - In our case, the coefficient of `duration` is **0.0123**.
