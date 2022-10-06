# SQL-Patika
Patika.dev'deki SQL derslerine ait ödevlerin bulunduğu repodur. 

**HOMEWORK-1** <br/>

*1.1*
```
SELECT title, description FROM film;
```

*1.2*
```
SELECT * FROM film
WHERE length > 60 AND length < 75;
```

*1.3*
```
SELECT * FROM film 
WHERE rental_rate = 0.99 AND (replacement_cost = 12.99 OR replacement_cost = 28.99);
```

*1.4*
```
SELECT last_name FROM customer 
WHERE first_name = 'Mary';
```

*1.5*
```
SELECT * FROM film
WHERE length < 50 AND (rental_rate != 2.99 AND rental_rate != 4.99);
```
**HOMEWORK-2** <br/>

*2.1*
```
SELECT * FROM film
WHERE replacement_cost BETWEEN 12.99 AND 16.99 AND (replacement_cost != 16.99);
```

*2.2*
```
SELECT first_name, last_name FROM actor
WHERE first_name IN ('Penelope', 'Nick', 'Ed');
```

*2.3*
```
SELECT * FROM film
WHERE rental_rate IN (0.99, 2.99, 4.99) AND replacement_cost IN (12.99, 15.99, 28.99);
```

**HOMEWORK-3** <br/>

*3.1*
```
SELECT country FROM country
WHERE country LIKE 'A%a';
```

*3.2*
```
SELECT country FROM country
WHERE country LIKE '%_____n';
```

*3.3*
```
SELECT title FROM film
WHERE title ILIKE 't%t%t%t%';
```

*3.4*
```
SELECT * FROM film 
WHERE title LIKE 'C%' AND length > 90 AND rental_rate IN (2.99);
```
