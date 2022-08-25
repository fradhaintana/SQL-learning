# SQL-learning
# I'm new to learn SQL.. but i'll share my work here.

SELECT name FROM sqlite_schema
WHERE type='table'
ORDER BY name;

PRAGMA table_info(tracks);

SELECT trackid, name, albumid, composer, unitprice FROM tracks;
SELECT name, milliseconds, albumid
FROM tracks ORDER BY albumid;

SELECT name, milliseconds, albumid
FROM tracks ORDER BY albumid ASC, milliseconds DESC;

SELECT DISTINCT city
FROM customers
ORDER BY city;

SELECT city
FROM customers
ORDER BY city;

SELECT name, milliseconds, bytes, albumid
FROM tracks
WHERE albumid = 1 AND milliseconds > 250000;

SELECT trackid, name
FROM tracks
LIMIT 10;

SELECT InvoiceId, BillingAddress, Total
FROM invoices
WHERE Total BETWEEN 14.91 AND 18.86
ORDER BY Total;

SELECT TrackId, Name, Mediatypeid
FROM tracks
WHERE mediatypeid IN (1,2)
ORDER BY name ASC;

SELECT trackid, name, composer
FROM tracks
WHERE composer IS NULL
ORDER BY name ASC
LIMIT 15;

SELECT albumid, COUNT(trackid)
FROM tracks
GROUP BY albumid
HAVING albumid=1;
