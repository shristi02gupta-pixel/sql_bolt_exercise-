Question 1-Find all the Toy Story movies 
Output 1-SELECT * FROM movies WHERE title LIKE 'Toy Story%';
Question 2- Find all the movies directed by John Lasseter
Output 2-SELECT * FROM movies WHERE director = 'John Lasseter';
Question 3-Find all the movies (and director) not directed by John Lasseter
Output 3-SELECT title, director FROM movies WHERE director <> 'John Lasseter';
Question 4-Find all the WALL-* movies
Output 4-SELECT * FROM movies WHERE title LIKE 'WALL-%';