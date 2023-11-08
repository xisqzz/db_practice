CREATE TABLE Students (
    StudentID SERIAL PRIMARY KEY,
    FirstName VARCHAR(50),
    LastName VARCHAR(50),
    Age INT
);


CREATE TABLE dealer (
    dealer_id SERIAL PRIMARY KEY,
  	dealer_city VARCHAR(50),
	dealer_brand VARCHAR(50),
	address VARCHAR(50)
);

CREATE TABLE auto (
    brand_id SERIAL PRIMARY KEY,
  	brand_auto VARCHAR(50),	
	count INTEGER,
	model VARCHAR(50),
	price INTEGER
);

CREATE TABLE characteristics (
     year SERIAL PRIMARY KEY,
	mileage INTEGER,
	car_body VARCHAR(50),
	drive_unit VARCHAR(50)
);

CREATE TABLE order (
     order_id SERIAL PRIMARY KEY,
	client_id INTEGER,
	dealer_id INTEGER,
	auto_id INTEGER
);

CREATE TABLE client (
     client_id SERIAL PRIMARY KEY,
	name VARCHAR(50),
	last_name VARCHAR(50),
	age INTEGER
);

INSERT INTO car_showroom (id, city, dealer, orders) VALUES 
(1, 'Москва', 'Автодилер Mazda', 0), (2, 'Москва', 'Автодилер Mercedes-Benz', 0),
(3, 'Москва', 'Автодилер Kia', 2), (4, 'Новосибирск', 'Автодилер Porshe', 2), (5, 'Новосибирск', 'Автодилер Kia', 0), (6, 'Новосибирск', 'Автодилер Tesla', 4)

INSERT INTO dealer (dealer_id, dealer_city, dealer_brand, address) 
VALUES (1, 'Москва', 'Mazda', 'Ломоносва 16'),
(2, 'Москва', 'Mercedes-Benz', 'Ленина 5'),
(3, 'Москва', 'Kia', 'Красный проспект 15'),
(4, 'Новосибирск', 'Porshe', 'Ленинградский проспект 5'),
(5, 'Новосибирск', 'Kia', 'Гоголя 1'),
(6, 'Новосибирск', 'Tesla', 'Мира 43')





