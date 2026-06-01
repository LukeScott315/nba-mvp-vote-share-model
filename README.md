
# NBA MVP Vote Share Model

This project builds and backtests a regression model to estimate the NBA MVP using historical NBA player stats and MVP voting results.

The model trains on seasons before the season being predicted, then tests on each year that was held out from 2015 through 2026.

You can also see a logical progression model by model. Model one used a lot of broad player statistics but was ultimately not very successful,
as team success was not taken into account and overlapping stats made coefficients inaccurate. Model 2 cleaned up stats and used a more specific
range and the model became less redundant, but it still ignored team success. Model 3 also took into account team success, and showed the most
accuracy (9 out of last 12), with the three misses being classic MVP model errors (especially with the "Jokic problem" when it comes to statistical
profiles).

## This Model
- Scrapes historical NBA player stats and MVP voting results from Basketball Reference
- Cleans player statistics
- Combines those player statistics with MVP voting data
- Builds a regression model to estimate MVP vote share
- Backtests predictions season by season (essentially testing the model and improving accuaracy and regression weights)
- Compares predicted MVP rankings to actual voting results

## Tools
- Python
- pandas
- scikit-learn
- Jupyter Notebook

## Project Notes
This project was built as a personal sports analytics project to practice data cleaning, regression modeling, backtesting, and interpreting model 
results in tbe NBA. It is not meant to be a definitive MVP formula. Even in the model's misses, we can have interesting takeaways. 

IMPORTANT: Some cells may take a minute to run because the notebook uses time.sleep between Basketball Reference requests. This is intentional and helps avoid sending requests too quickly while scraping data.
