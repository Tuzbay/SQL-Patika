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

**HOMEWORK-4** <br/>

*4.1*
```
SELECT DISTINCT replacement_cost FROM film;
```

*4.2*
```
SELECT COUNT(DISTINCT replacement_cost) FROM film;
```

*4.3*
```
SELECT COUNT(*) FROM film
WHERE title LIKE 'T%' AND rating IN ('G');
```

*4.4*
```
SELECT COUNT(country) FROM country
WHERE country LIKE '_____';
```

*4.5*
```
SELECT COUNT(city) FROM city
WHERE city ILIKE '%R';
```

**HOMEWORK-5** <br/>

*5.1*
```
SELECT title, length FROM film
WHERE title LIKE '%n'
ORDER BY length DESC
LIMIT 5;
```

*5.2*
```
SELECT title, length FROM film
WHERE title LIKE '%n'
ORDER BY length
OFFSET 5
LIMIT 5;
```

*5.3*
```
SELECT last_name, store_id FROM customer
WHERE store_id = 1
ORDER BY last_name DESC
LIMIT 4;
```

**HOMEWORK-6** <br/>

*6.1*
```
SELECT ROUND(AVG(rental_rate), 2) FROM film;
```

*6.2*
```
SELECT COUNT(title) FROM film
WHERE title LIKE 'C%';
```

*6.3*
```
SELECT MAX(length) FROM film
WHERE rental_rate = 0.99;
```

*6.4*
```
SELECT COUNT(DISTINCT replacement_cost)
FROM film
WHERE length > 150;
```

**HOMEWORK-7** <br/>

*7.1*
```
SELECT rating, COUNT(title) FROM film
GROUP BY rating;
```

*7.2*
```
SELECT replacement_cost, COUNT(title)
FROM film
GROUP BY replacement_cost
HAVING 50 < COUNT(title)
ORDER BY COUNT(title) ASC;
```

*7.3*
```SELECT store_id, COUNT(customer_id)
FROM customer
GROUP BY store_id
ORDER BY store_id;
```

*7.4*
```
SELECT country_id, COUNT(city_id) 
FROM city
GROUP BY country_id
ORDER BY COUNT(city_id) DESC
LIMIT 1;
```

**HOMEWORK-8** <br/>

*8.1*
```
CREATE TABLE employee (ACTION
	id INTEGER,
	name VARCHAR(50),
	birthday DATE,
	email VARCHAR(100)
);
```

*8.2*
```
insert into employee (id, name, birthday, email) values (1, 'Robbi', '1913-11-10', 'rgaythor0@earthlink.net');
insert into employee (id, name, birthday, email) values (2, 'Archambault', '1996-10-27', 'achue1@elegantthemes.com');
insert into employee (id, name, birthday, email) values (3, 'Jennette', '1936-04-08', 'jbrownsell2@bloomberg.com');
insert into employee (id, name, birthday, email) values (4, 'Denyse', '1973-03-02', 'dnorthway3@webeden.co.uk');
insert into employee (id, name, birthday, email) values (5, 'Caresa', '1982-05-08', 'conions4@opensource.org');
insert into employee (id, name, birthday, email) values (6, 'Sarita', '1951-09-14', 'sprinne5@hc360.com');
insert into employee (id, name, birthday, email) values (7, 'Lionel', '1971-06-13', 'lgittens6@kickstarter.com');
insert into employee (id, name, birthday, email) values (8, 'Rivi', '1936-10-16', 'rpurchon7@vimeo.com');
insert into employee (id, name, birthday, email) values (9, 'Jordanna', '1929-01-08', 'jpinard8@ft.com');
insert into employee (id, name, birthday, email) values (10, 'Millie', '1989-05-07', 'mbauer9@g.co');
insert into employee (id, name, birthday, email) values (11, 'Hewitt', null, 'hgouta@columbia.edu');
insert into employee (id, name, birthday, email) values (12, 'Avril', '1911-05-11', 'acoopmanb@microsoft.com');
insert into employee (id, name, birthday, email) values (13, 'Nicolle', '1924-04-22', 'nsabbatierc@epa.gov');
insert into employee (id, name, birthday, email) values (14, 'Wini', '1954-04-07', 'wspellecyd@nyu.edu');
insert into employee (id, name, birthday, email) values (15, 'Benn', '1985-08-22', 'bsandhille@telegraph.co.uk');
insert into employee (id, name, birthday, email) values (16, 'Trixi', '1984-12-09', 'tnodesf@ocn.ne.jp');
insert into employee (id, name, birthday, email) values (17, 'Reider', '2022-07-21', 'rplaydong@engadget.com');
insert into employee (id, name, birthday, email) values (18, 'Maureen', '1914-06-15', 'mdairtonh@dion.ne.jp');
insert into employee (id, name, birthday, email) values (19, 'Rhody', '1925-10-18', 'rcolreini@ftc.gov');
insert into employee (id, name, birthday, email) values (20, 'Tessa', '1938-09-17', 'tdallowj@economist.com');
insert into employee (id, name, birthday, email) values (21, 'Lemuel', '1918-05-30', 'ltrevettk@photobucket.com');
insert into employee (id, name, birthday, email) values (22, 'Marlene', '1970-05-21', 'mlearoydl@ustream.tv');
insert into employee (id, name, birthday, email) values (23, 'Sabine', '2012-04-18', 'sjaycockm@hostgator.com');
insert into employee (id, name, birthday, email) values (24, 'Grace', '1974-01-24', 'gcreeboen@yellowbook.com');
insert into employee (id, name, birthday, email) values (25, 'Marcela', '1911-09-23', 'mfurneauxo@over-blog.com');
insert into employee (id, name, birthday, email) values (26, 'Arlinda', '1952-04-03', 'afoanp@xinhuanet.com');
insert into employee (id, name, birthday, email) values (27, 'Bobby', '1969-11-18', 'bwileq@eepurl.com');
insert into employee (id, name, birthday, email) values (28, 'Abe', '2004-12-26', 'abradneckr@techcrunch.com');
insert into employee (id, name, birthday, email) values (29, 'Malory', '1955-04-29', 'mlinchs@nyu.edu');
insert into employee (id, name, birthday, email) values (30, 'Angie', '2017-12-23', 'aleversucht@go.com');
insert into employee (id, name, birthday, email) values (31, 'Tomkin', null, 'tadlardu@prlog.org');
insert into employee (id, name, birthday, email) values (32, 'Amalia', '1953-11-29', 'asouthcoatv@dailymotion.com');
insert into employee (id, name, birthday, email) values (33, 'Charil', '1933-06-29', 'ckhomishinw@samsung.com');
insert into employee (id, name, birthday, email) values (34, 'Karrie', '2022-09-23', 'kchatainx@ibm.com');
insert into employee (id, name, birthday, email) values (35, 'Alberik', '1909-02-27', 'acreigany@blogger.com');
insert into employee (id, name, birthday, email) values (36, 'Aleece', null, 'abirtchnellz@homestead.com');
insert into employee (id, name, birthday, email) values (37, 'Rodrigo', null, 'rscaice10@cargocollective.com');
insert into employee (id, name, birthday, email) values (38, 'Kellsie', '1910-09-06', 'ksiggens11@blogspot.com');
insert into employee (id, name, birthday, email) values (39, 'Bertram', null, 'barlidge12@nature.com');
insert into employee (id, name, birthday, email) values (40, 'Suzie', '1921-07-25', 'sblaylock13@nsw.gov.au');
insert into employee (id, name, birthday, email) values (41, 'Norean', '2008-12-05', null);
insert into employee (id, name, birthday, email) values (42, 'Boy', '1924-11-28', 'brolfo15@nydailynews.com');
insert into employee (id, name, birthday, email) values (43, 'Theobald', '1971-05-19', 'thackey16@tuttocitta.it');
insert into employee (id, name, birthday, email) values (44, 'Petronia', '1982-02-10', null);
insert into employee (id, name, birthday, email) values (45, 'Franni', '1997-06-13', 'fjelk18@themeforest.net');
insert into employee (id, name, birthday, email) values (46, 'Kayley', '1903-10-10', 'kcarnson19@arizona.edu');
insert into employee (id, name, birthday, email) values (47, 'Alleyn', '1970-02-12', 'awollers1a@google.ru');
insert into employee (id, name, birthday, email) values (48, 'Gwynne', '2004-12-03', 'gpallin1b@discuz.net');
insert into employee (id, name, birthday, email) values (49, 'Theodora', '1959-07-23', 'tosculley1c@cnn.com');
insert into employee (id, name, birthday, email) values (50, 'Lynn', null, 'louthwaite1d@newsvine.com');
```

*8.3*
```
UPDATE employee 
	SET name = 'Tunay Uzbay YELCE',
		birthday = '1997-03-29',
		email = 't.uzbayyelce@gmail.com'
	WHERE id = 1;

UPDATE employee 
	SET name = 'Hikmethan Can',
		birthday = '1997-06-22',
		email = 'hikmethan@gmail.com'
	WHERE id = 2;
	

UPDATE employee 
	SET name = 'Mehmet Tuzcu',
		birthday = '1997-09-30',
		email = 'mehmettuzcu@gmail.com'
	WHERE id = 3;

UPDATE employee 
	SET name = 'İbrahim Yağmur',
		birthday = '1998-10-07',
		email = 'ibrahimyagmur@gmail.com'
	WHERE id = 4;

UPDATE employee 
	SET name = 'Muhammed Çoşut',
		birthday = '1998-04-14',
		email = 'muhammedcosut@gmail.com'
	WHERE id = 5;
```

*8.4*
```
DELETE FROM employee
WHERE id IN (10,11,12,13,14)
RETURNING *;
```
