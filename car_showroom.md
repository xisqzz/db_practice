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

