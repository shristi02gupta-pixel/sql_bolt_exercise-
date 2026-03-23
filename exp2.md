Question 1-Find the movie with a row id of 6
Output 1-SELECT *FROM movies WHERE id = 6;
Question 2-Find the movies released in the years between 2000 and 2010
Output 2- SELECT *FROM movies WHERE year BETWEEN 2000 AND 2010;
Question 3-Find the movies not released in the years between 2000 and 2010
Output 3-SELECT *FROM movies WHERE year NOT BETWEEN 2000 AND 2010;
Question 4-Find the first 5 Pixar movies and their release year
Output 4-SELECT title, year FROM movies ORDER BY year ASC LIMIT 5;
