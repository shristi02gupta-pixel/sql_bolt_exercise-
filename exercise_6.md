# sqlboltexercise
---> Exercise 6: JOIN & Filtering
---

### Question:1 Find the domestic and international sales for each movie

```sql id="q1j6kp"
SELECT m.title, b.domestic_sales, b.international_sales
FROM movies m
JOIN boxoffice b
ON m.id = b.movie_id;
```

| Title               | Domestic Sales | International Sales |
| ------------------- | -------------- | ------------------- |
| Finding Nemo        | 380843261      | 555900000           |
| Monsters University | 268492764      | 475066843           |
| Ratatouille         | 206445654      | 417277164           |
| Cars 2              | 191452396      | 368400000           |
| Toy Story 2         | 245852179      | 239163000           |
| The Incredibles     | 261441092      | 370001000           |
| WALL-E              | 223808164      | 297503696           |
| Toy Story 3         | 415004880      | 648167031           |
| Toy Story           | 191796233      | 170162503           |
| Cars                | 244082982      | 217900167           |
| Up                  | 293004164      | 438338580           |
| Monsters, Inc.      | 289916256      | 272900000           |
| A Bug's Life        | 162798565      | 200600000           |
| Brave               | 237283207      | 301700000           |

---

### Question:2 Show the sales numbers for each movie that did better internationally rather than domestically

```sql id="z9d3lx"
SELECT m.title, b.domestic_sales, b.international_sales
FROM movies m
JOIN boxoffice b
ON m.id = b.movie_id
WHERE b.international_sales > b.domestic_sales;
```

| Title               | Domestic Sales | International Sales |
| ------------------- | -------------- | ------------------- |
| Finding Nemo        | 380843261      | 555900000           |
| Monsters University | 268492764      | 475066843           |
| Ratatouille         | 206445654      | 417277164           |
| Cars 2              | 191452396      | 368400000           |
| The Incredibles     | 261441092      | 370001000           |
| WALL-E              | 223808164      | 297503696           |
| Toy Story 3         | 415004880      | 648167031           |
| Up                  | 293004164      | 438338580           |
| A Bug's Life        | 162798565      | 200600000           |
| Brave               | 237283207      | 301700000           |

---

### Question:3 List all the movies by their ratings in descending order

```sql id="8c4gms"
SELECT m.title, b.rating
FROM movies m
JOIN boxoffice b
ON m.id = b.movie_id
ORDER BY b.rating DESC;
```

| Title               | Rating |
| ------------------- | ------ |
| WALL-E              | 8.5    |
| Toy Story 3         | 8.4    |
| Toy Story           | 8.3    |
| Up                  | 8.3    |
| Finding Nemo        | 8.2    |
| Monsters, Inc.      | 8.1    |
| Ratatouille         | 8.0    |
| The Incredibles     | 8.0    |
| Toy Story 2         | 7.9    |
| Monsters University | 7.4    |
| Cars                | 7.2    |
| A Bug's Life        | 7.2    |
| Brave               | 7.2    |
| Cars 2              | 6.4    |

---
