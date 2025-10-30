# Golden Era of Video Games

## Project Overview

According to Mordor Intelligence, video games are big business: the global gaming market is projected to be worth more than $300 billion by 2027. With so much money at stake, major game publishers are hugely incentivized to create the next big hit. But are games getting better, or has the golden age of video games already passed?

In this project, we'll analyze video game critic and user scores, in addition to sales data for the top 400 video games released since 1977. You'll search for a golden age of video games by identifying release years that users and critics liked best, and you'll explore the business side of gaming by looking at game sales data.

## Tasks

1. Analyze the average critic and user scores for each year.
2. Identify years where critics and users broadly agreed on high ratings.
3. Explore sales data in relation to critic and user scores.
4. Determine the years that represent the "golden era" of video games based on the analysis.

## Skills Highlighted

This project showcases the following SQL skills:

- **Data Aggregation**: Using `AVG()` to calculate average scores and `COUNT()` to determine the number of games released per year.
  
- **Joins**: Employing `INNER JOIN` to combine data from multiple tables, such as `game_sales`, `reviews`, `users_avg_year_rating`, and `critics_avg_year_rating`.

- **Filtering and Grouping**: Utilizing `WHERE` and `HAVING` clauses to filter results based on specific criteria (e.g., years with high average scores) and grouping data using `GROUP BY`.

- **Calculating Differences**: Creating new calculated fields, such as the difference between average critic and user scores.

- **Ordering Results**: Using `ORDER BY` to sort results based on specific columns, facilitating easier interpretation of data.
