## Movie Analysis


### Overview
This Python project aims to find correlations between various movie features such as name, rating, genre, year, released, score, votes, director, writer, star, country, budget, gross, company, and runtime.

### Data Preprocessing
Before conducting the correlation analysis, the following data preprocessing steps were performed:

* Check for Missing Data
Missing data can hinder accurate analysis. The dataset was carefully examined for any missing values in each column. For columns with missing data, we applied appropriate strategies to handle them.

* Drop Missing Values
As some old movies might lack budget information and certain other fields, we decided to drop rows with missing values to ensure consistency in the analysis.

* Change Data Types
To remove decimal numbers from columns with monetary amounts (budget and gross), we converted these columns to integer data types. This ensures better compatibility and enhances the correlation calculations.

* Create a New Column for Release Year Matching
The original data tended to have different values for the movie release year (released) and the movie year (year) in some cases. To align these values, we created a new column called release_year_matched, which holds the year extracted from the released date. This allows for a more accurate analysis of movie trends over time.

* Categorize Non-Numeric Values
Certain movie features, such as genre, country, director, writer, and star, contain non-numeric values. To include them in the correlation analysis, we performed a categorical mapping, assigning numeric codes to each unique value in these columns. This step enables the correlation of non-numeric features with other numeric attributes.

* EDA (Exploratory Data Analysis)
During the Exploratory Data Analysis phase, in addition to the mentioned correlations, we made the following observations:

* Genre Distribution:
We analyzed the distribution of movies across different genres and identified the most common and rare genres.

* Top Directors and Writers:
Explored the directors and writers with the highest number of movie credits, helping identify influential filmmakers in the dataset.

* Country-wise Movie Production:
Investigated the distribution of movies based on their production countries, revealing which countries have contributed the most to the dataset.

* Correlation Matrix
The correlation matrix plot (see movie_correlation.png) provides a visual representation of the correlation coefficients between various movie features. The values closer to 1 indicate a strong positive correlation, while values closer to -1 indicate a strong negative correlation. Correlation values close to 0 suggest a weak or no correlation.

### Conclusion
Based on the analysis, we discovered significant positive correlations between votes and gross revenue, as well as between budget and gross revenue. These findings align with the common understanding that popular movies with higher budgets tend to generate more revenue.

The preprocessing steps, including handling missing data, aligning release years, and categorizing non-numeric values, ensured the dataset's cleanliness and consistency, enabling a more reliable analysis.

### Future Work
This project represents only a preliminary analysis of the movie dataset. Further investigation can be carried out to explore other potential correlations and build predictive models to forecast a movie's success based on its features. Additionally, we can use machine learning algorithms to gain deeper insights into the factors influencing a movie's revenue and popularity.

Feel free to contribute to this project, raise issues, or suggest improvements. Let's keep enhancing our understanding of movie industry trends through data-driven insights!



#### Acknowledgments
Special thanks to all contributors who helped collect and clean the movie dataset, and to the open-source community for their valuable libraries and tools.

If you have any questions or suggestions, feel free to reach out or open an issue. Happy coding!
