Change the query shown so that it displays Nobel prizes for 1950.

```SQL
SELECT yr, subject, winner
  FROM nobel
 WHERE yr = 1950
```

Show who won the 1962 prize for literature.

```SQL
SELECT winner
  FROM nobel
 WHERE yr = 1962
   AND subject = 'literature'

```
