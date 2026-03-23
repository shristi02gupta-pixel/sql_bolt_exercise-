# sqlboltexercise
---> Exercise 4: DISTINCT, ORDER BY & LIMIT
---

### Question:1 List all directors of Pixar movies (alphabetically), without duplicates

```sql id="b2r6ht"
SELECT DISTINCT director
FROM movies
ORDER BY director ASC;
```

| Director       |
| -------------- |
| Andrew Stanton |
| Brad Bird      |
| Brenda Chapman |
| Dan Scanlon    |
| John Lasseter  |
| Lee Unkrich    |
| Pete Docter    |

---

### Question:2 List the last four Pixar movies released (ordered from most recent to least)

```sql id="8v3qjm"
SELECT * FROM movies
ORDER BY year DESC
LIMIT 4;
```

| ID | Title               | Director       | Year | Length (Minutes) |
| -- | ------------------- | -------------- | ---- | ---------------- |
| 14 | Monsters University | Dan Scanlon    | 2013 | 110              |
| 13 | Brave               | Brenda Chapman | 2012 | 102              |
| 12 | Cars 2              | John Lasseter  | 2011 | 120              |
| 11 | Toy Story 3         | Lee Unkrich    | 2010 | 103              |

---

### Question:3 List the first five Pixar movies sorted alphabetically

```sql id="7m4kxs"
SELECT * FROM movies
ORDER BY title ASC
LIMIT 5;
```

| ID | Title        | Director       | Year | Length (Minutes) |
| -- | ------------ | -------------- | ---- | ---------------- |
| 2  | A Bug's Life | John Lasseter  | 1998 | 95               |
| 13 | Brave        | Brenda Chapman | 2012 | 102              |
| 7  | Cars         | John Lasseter  | 2006 | 117              |
| 12 | Cars 2       | John Lasseter  | 2011 | 120              |
| 5  | Finding Nemo | Andrew Stanton | 2003 | 107              |

---

### Question:4 List the next five Pixar movies sorted alphabetically

```sql id="g1xq9v"
SELECT * FROM movies
ORDER BY title ASC
LIMIT 5 OFFSET 5;
```

| ID | Title               | Director      | Year | Length (Minutes) |
| -- | ------------------- | ------------- | ---- | ---------------- |
| 4  | Monsters, Inc.      | Pete Docter   | 2001 | 92               |
| 14 | Monsters University | Dan Scanlon   | 2013 | 110              |
| 8  | Ratatouille         | Brad Bird     | 2007 | 115              |
| 1  | Toy Story           | John Lasseter | 1995 | 81               |
| 3  | Toy Story 2         | John Lasseter | 1999 | 93               |

---
