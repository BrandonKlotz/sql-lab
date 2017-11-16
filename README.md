# sql-lab

SQL Queries

Select all the records from the "Customers" table.
```SELECT * FROM customers;```

Get distinct countries from the Customers table.
```SELECT DISTINCT country FROM customers;```

Get all the records from the table Customers where the Customer’s ID starts with “BL”.
```SELECT * FROM customers WHERE customerid LIKE 'BL%';```

Get the first 100 records of the orders table.
```SELECT * FROM orders LIMIT 100;```

Get all customers that live in the postal codes 1010, 3012, 12209, and 05023.
```SELECT * FROM customers WHERE postalcode IN ('1010', '3012', '12209', '05023');```

Get all orders where the ShipRegion is not equal to NULL.
```SELECT * FROM orders WHERE shipregion IS NULL;```

Get all customers ordered by the country, then by the city.
```SELECT * FROM customers ORDER BY country, city;```

Add a new customer to the customers table. You can use whatever values. 
```INSERT INTO customers(customerid, companyname, contactname, contacttitle, address, city, region, postalcode, country, phone, fax) values('JMULCC', 'Comedy Central', 'John Mulaney', 'Comedian', '3344 Laugh Lane', 'Los Angelos', 'CA', '09919', 'United States', '617-002-1100','617-102-1101');```

Update all ShipRegion to the value EuroZone in the Orders table, where the ShipCountry is equal to France.
```UPDATE orders SET shipcountry='EuroZone' WHERE shipcountry='France';```

Delete all orders from order_details that have quantity of 1.
```DELETE FROM order_details WHERE quantity=1;```
```SELECT * FROM order_details WHERE quantity=1;```

Calculate the average, max, and min of the quantity at the order details table.
```SELECT AVG(quantity) FROM order_details;```
```SELECT MAX(quantity) FROM order_details;```
```SELECT MIN(quantity) FROM order_details;```

Calculate the average, max, and min of the quantity at the order details table,
grouped by the orderid.
```SELECT AVG(quantity), MAX(quantity), MIN(quantity), orderid FROM order_details GROUP BY orderid;```

Find the CustomerID that placed order 10290 (orders table).
```SELECT customerid FROM orders WHERE orderid=10290;```

DO an inner join, left join, right join on orders and customer tables.
```SELECT * FROM orders INNER JOIN customers ON orders.customerid = customers.customerid;```
```SELECT * FROM orders LEFT JOIN customers ON orders.customerid = customers.customerid;```
```SELECT * FROM orders RIGHT JOIN customers ON orders.customerid = customers.customerid;```

Get employees firstname for all employees who report to no one.
```SELECT * FROM employees WHERE reportsto IS NULL;```

Get employees firstname for all employees who report to no one.
```SELECT * FROM employees WHERE reportsto=2;```
