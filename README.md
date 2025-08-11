# Streaming-Platform-Analysis
**Goal**: The goal is to analyze TV shows from 4 streaming platforms (Netflix, Prime Video, Hulu, and Disney+) to:
1. Identify which streaming service has the highest-rated shows.
2. Explore whether IMDb ratings can be predicted using other features.

## Tools & Technologies
- Python: pandas, scikit-learn, seaborn, and matplotlib for data cleaning, visualization, and modeling.
- RandomForestRegressor for regression modeling.

## Dataset
- Source:"tv_shows.csv" from Kaggle
- 5,611 original titles, reduced to 3,316 titles after cleaning

## Data Cleaning
- Removed the bottom 40% of shows, to avoid low-review bias
- Dropped null values in IMDb & Rotten Tomatoes
- Dropped unused columns: `Unnamed: 0`, `type`
- Converted `Age Rating` and `Rotten Tomatoes` from string to numeric
- Renamed columns for clarity

## Visualizations
1. Boxplot & Swarmplot: IMDb ratings distribution per streaming service
2. Bar Graph: Top 50 shows per platform
3. Correlation Heatmap: Relationships between IMDb and other features

## Machine Learning Model 
- Model: RandomForestRegressor
- Goal: Predict IMDb ratings from Rotten Tomatoes, Age Rating, and Release Year
- Best depth: 4 (minimized Mean Absolute Error)
- R² score: 0.35 (moderate predictability)
- Meam Absolute Error: 0.47 (small average rating difference)

## Findings
- Netflix had the highest average IMDb rating (7.52/10) and almost half of the top 50 shows.
- 'Rotten Tomatoes' is the strongest predictor of IMDb ratings, with a moderate relationship.
- Limited Rotten Tomatoes data (only 18% coverage) and missing genres restricted model accuracy.

## Files
- Jupyter Notebook: "Final Presentation Spring 2025 Final Draft.ipynb"
- Dataset: "tv_shows.csv"
- Report & Visuals: "Final_IMDbRatings_Report.docx" & "Final Presentation Spring 2025 Final.pdf"
