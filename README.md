# Analysis for Maximizing Box Office Success in the Movie Industry
### Author: Loyce Tsuma


![Screenshot 2024-07-24 133806](https://github.com/user-attachments/assets/a502a961-2319-4514-8c13-6f318b0a4646)


## Overview

The exploratory data analysis aims to identify successful movie genres and trends to provide actionable recommendations for a new movie studio, enhancing box office success.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Business Problem

1.Identify Top Genres: Determine which movie genres (e.g., action, comedy, drama) are currently leading at the box office to prioritize film production for commercial success.

2.Recognize Emerging Trends: Spot new or growing trends in the movie industry to capitalize on popular categories by developing relevant films.

3.Understand Audience Preferences: Analyze audience demographics and movie-going habits to tailor the film slate to the preferences of core target audiences.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### The Data

The Data was collected from combined two data sets 

`im.db.zip` a * Zipped SQLite database  and * `bom.movie_gross.csv.gz`

The dataset contains 3025 records, each representing a movie id.

The distinct column(unique identifier) in this dataframe is the `movie_id`

Data was cleaned and and stored in a file  `movie_data.csv` which details movie details in columns  `genres`,`original_title`,`start_year`,`runtime_minutes`	`averagerating`,`numvotes`,`studio`,`domestic_gross` and `foreign_gross`.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Findings

**Identifying Top-Performing Genres.**
  
There are 20 Genres

The most profitable genre is Adventure,followed by Action,Drama,Comedy,Animation respectively

The genre with the least revenue is News and Western and Musicals

The studio should prioritize creating films in the profitable genres to increase their chances of commercial success.


  <img width="1000" alt="image" src="https://github.com/user-attachments/assets/a83d9903-b234-4e55-ac0b-f43107512cf9">



**Understanding Target Audience Preferences.**
  
- Genre Popularity

We analyze how different genres perform in terms of total gross revenue

  <img width="300" alt="image" src="https://github.com/user-attachments/assets/2fe3ad90-af8b-427a-9b3c-b323d545393c">


- Corelation between rating and revenue

We checked the average rating for each genre to see if higher-rated genres correlate with higher revenues using statistical methods as well as visualizations

  <img width="900" alt="image" src="https://github.com/user-attachments/assets/0fb7e91d-e4f2-4be4-b2bd-e64b6405235e">

Observation

We note no visible correlation between the `Average Rating` and ` Gross Revenue`

The correlation coefficient of -0.29 suggests a weak negative relationship between average ratings and total gross revenue, but the p-value of 0.19 indicates that this relationship is not statistically significant, implying it may be due to random chance.

- Audience Engagement

We analyze the number of votes to gauge audience engagement with different genres,knowing which genres are popular will allow the studio and 
distributors to tailor their marketing strategies,if a particular genre is trending, marketing campaigns can be focused on that genre to attract more viewers. 

  <img width="1000" alt="image" src="https://github.com/user-attachments/assets/c248183d-a65b-49b6-8f85-36a0e6095122">


Observation

The Scify and Adventure genres are very popular this means that the studio should focus on these two when doing targeted marketing

**Analyzing Emerging Market Trends.**
- Runtime Analysis
  
Investigated if there's a correlation between runtime and movie success through statistical methods.

  <img width="600" alt="image" src="https://github.com/user-attachments/assets/02a1ef2a-bd9e-4866-8f09-2ba57bbf337a">

Observation

The linear regression analysis yields a constant term of approximately -$77,657,490  which serves as a baseline for the model, and a coefficient for runtime of about $1,615,703 indicating that for each additional minute of runtime, total gross revenue is expected to increase by this amount, assuming all other factors are constant. 

This positive relationship suggests that longer films tend to generate higher box office earnings, and for instance, a 10-minute increase in runtime could lead to an expected revenue increase of approximately $16,157,030. 

The regression equation can be summarized as:

Total Gross=−77,657,490+1,615,703×Runtime Minutes

- Competitor Intelligence
  
Observation
BV,FOX,UNI,WB and Sony are the top 5 income generating studios this are the main competitors in the movie industry

We also note that 2019 posted the lowest revenue and this could be attributed to Covid 19 pandemic,Generally the movie industry has been on an upward trajectory commercially

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Recommendations

1.To maximize commercial success, the new movie studio should prioritize creating films in top-performing genres like Adventure, Action, Drama, Comedy, and Animation

2.Avoid Low-Performing Genres

Genres such as News, Western, and Musicals have shown the least revenue.

It is advisable to minimize investment in these categories unless a unique concept can be developed.

3.Capitalize on emerging trends in Sci-Fi and Adventure

The growing popularity of Sci-Fi and Adventure genres presents an opportunity for the studio.

Targeted marketing efforts should be directed towards these genres to attract audiences looking for fresh content.

4.Consider runtime when developing scripts

The analysis reveals a weak positive correlation between runtime and total gross revenue, suggesting that longer films may perform better.

The studio should consider this when developing scripts and production plans, aiming for runtimes that align with successful films in the targeted genres.

5.Tailor film offerings to audience demographics

Monitor ratings and revenue correlation, recognizing its weak negative relationship and lack of statistical significance

The observed weak negative correlation (-0.29) between average ratings and total gross revenue indicates that higher-rated movies do not necessarily lead to higher revenue.
Statistical Significance: With a p-value of 0.19, the correlation is not statistically significant, suggesting that the relationship between ratings and revenue could be influenced by random chance. Therefore, while ratings are important, they should not be the sole determinant in film selection.
The studio should focus on quality but also consider other factors, such as marketing and release timing, that can influence box office success.

Engagement Strategies:Use insights from audience engagement metrics to inform marketing strategies, ensuring that promotional efforts are aligned with the preferences of the target demographic.

Strategically time movie releases during optimal periods to boost box office performance.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Conclusion
By focusing on high-performing genres, leveraging emerging trends, understanding audience preferences, and strategically timing releases, the new movie studio can enhance its potential for commercial success.

Continuous monitoring of industry trends and audience feedback will further refine the studio's approach, ensuring that it remains competitive in the dynamic film industry.

