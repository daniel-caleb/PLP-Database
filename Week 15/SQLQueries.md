# The Mission:

## 1. Data Dive (10 pts):

Pick my dataset which was netflix_titles.csv

### Difficulties
- Inconsistent Data Entries. The dataset contains inconsistent or missing entries, especially in columns like Director, Cast, and Country, where some fields are blank.
- Categorical Diversity. The Listed in column contains multiple genres per entry, which can make it challenging to filter or group data by a single genre.

### Interesting Observation:
- The dataset contains a variety of content from different countries. This diversity can be explored to see which genres or types of content are prevalent in different regions.


## 2. Data Fun (20 pts):

- Most Popular Genres - Used the COUNT function to determine which genres are most popular.

```
SELECT listed_in, COUNT(*) AS Count
FROM netflix_titles
GROUP BY listed_in
ORDER BY Count DESC
LIMIT 5;
```

- Average Duration of Shows

```
SELECT AVG(duration) AS Avgduration
FROM netflix_titles;
```

## 3. Ask Away (30 pts):

-  What are the top-rated shows in the dataset? (Ordered by rating)
  
```
SELECT title, rating
FROM netflix_titles
ORDER BY rating DESC
LIMIT 10;
```

** You’ll get the titles and ratings of the highest-rated shows. **

- What are the top 5 countries producing the most Netflix shows?
  
```
SELECT country, COUNT(*) AS ShowCount
FROM netflix_titles
GROUP BY country
ORDER BY ShowCount DESC
LIMIT 5;
```

** This query will reveal the top 5 countries with the most shows. **