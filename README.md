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

Show the year, subject, and name of physics winners for 1980 together with the chemistry winners for 1984.

```SQL
SELECT *
FROM nobel
where (subject = "Physics" and yr = 1980) OR (subject = "Chemistry" and yr = 1984)
```


Show the year, subject, and name of winners for 1980 excluding chemistry and medicine

```SQL
SELECT *
FROM nobel
WHERE yr = 1980 AND NOT (subject = "chemistry" OR subject = "medicine")
```

outra forma de fazer

```SQL
SELECT * from nobel
WHERE yr = 1980
and subject NOT IN ('chemistry','medicine')
```

Show year, subject, and name of people who won a 'Medicine' prize in an early year (before 1910, not including 1910) together with winners of a 'Literature' prize in a later year (after 2004, including 2004)

```SQL
SELECT * 
FROM nobel
WHERE (subject = "Medicine" and yr < 1910) OR (subject = "literature" and yr >= 2004)
```
