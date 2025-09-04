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

Show all details of the presidential winners:

- Theodore Roosevelt
- Thomas Woodrow Wilson
- Jimmy Carter
- Barack Obama

```SQL
SELECT * FROM nobel
 WHERE winner in ('Theodore Roosevelt','Thomas Woodrow Wilson','Jimmy Carter','Barack Obama')
```

Show the winners with first name John

```SQL
SELECT winner 
FROM nobel
WHERE winner like ('John%')
```
