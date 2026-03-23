# sqlboltexercise
---> Exercise 5: Filtering, Sorting & LIMIT (Cities Data)
---

### Question:1 List all the Canadian cities and their populations

```sql id="6kz2lp"
SELECT city, population
FROM north_american_cities
WHERE country = 'Canada';
```

| City     | Population |
| -------- | ---------- |
| Toronto  | 2795060    |
| Montreal | 1717767    |

---

### Question:2 Order all the cities in the United States by their latitude from north to south

```sql id="8zt1wr"
SELECT city, latitude
FROM north_american_cities
WHERE country = 'United States'
ORDER BY latitude DESC;
```

| City         | Latitude  |
| ------------ | --------- |
| Chicago      | 41.878114 |
| New York     | 40.712784 |
| Philadelphia | 39.952584 |
| Los Angeles  | 34.052234 |
| Phoenix      | 33.448377 |
| Houston      | 29.760427 |

---

### Question:3 List all the cities west of Chicago, ordered from west to east

```sql id="j3x8qp"
SELECT city, longitude
FROM north_american_cities
WHERE longitude < -87.629798
ORDER BY longitude ASC;
```

| City                | Longitude   |
| ------------------- | ----------- |
| Los Angeles         | -118.243685 |
| Phoenix             | -112.074037 |
| Guadalajara         | -103.349609 |
| Mexico City         | -99.133208  |
| Ecatepec de Morelos | -99.050674  |
| Houston             | -95.369803  |

---

### Question:4 List the two largest cities in Mexico (by population)

```sql id="z9m2av"
SELECT city, population
FROM north_american_cities
WHERE country = 'Mexico'
ORDER BY population DESC
LIMIT 2;
```

| City                | Population |
| ------------------- | ---------- |
| Mexico City         | 8555500    |
| Ecatepec de Morelos | 1742000    |

---

### Question:5 List the third and fourth largest cities (by population) in the United States

```sql id="t4x9bd"
SELECT city, population
FROM north_american_cities
WHERE country = 'United States'
ORDER BY population DESC
LIMIT 2 OFFSET 2;
```

| City    | Population |
| ------- | ---------- |
| Chicago | 2718782    |
| Houston | 2195914    |

---
