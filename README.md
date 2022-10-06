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
