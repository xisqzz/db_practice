CREATE TABLE car_showroom (id SERIAL PRIMARY KEY, city VARCHAR(50), dealer VARCHAR(50), orders INTEGER)


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

CREATE TABLE orders (
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

INSERT INTO auto (brand_id, brand_auto, count, model, price) VALUES 
(1, 'Mazda', 10, 'RX-8', 800000),(2, 'Mercedes-Benz', 6, 'S-Class', 2000000), (3, 'Kia', 20, 'Rio', 1000000),
(4, 'Porshe', 2, '911', 13000000), (5, 'Kia', 7, 'Octawia', 700000),
(6, 'Tesla', 10, 'Model-y', 5000000)

INSERT INTO characteristics (year, mileage, car_body, drive_unit) VALUES 
(2008, 10000, 'full', 'sedan'), (2016, 100000, 'full', 'sedan'), (2005, 250000, 'rear', 'sedan'),
(2022, 1000, 'full', 'sedan'), (2010, 300000, 'rear', 'sedan'), (2000, 400000, 'front', 'sedan')

INSERT INTO client (client_id, name, last_name, age) VALUES 
(1, 'Артем', 'Митраков', 19), (2, 'Матвей', 'Мельников', 30), (3, 'Давид', 'Килин', 66),
(4, 'Иван', 'Джигирис', 18)

trigger 6: identify clients with age over 25 interested in sedans 

CREATE OR REPLACE FUNCTION identify_clients()
RETURNS TRIGGER AS $$
BEGIN
    IF NEW.age > 25 THEN
        INSERT INTO interested_clients (client_id)
        VALUES (NEW.client_id);
    END IF;
    RETURN NEW;
END;
$$ LANGUAGE plpgsql;

CREATE TRIGGER after_insert_client
AFTER INSERT ON client
FOR EACH ROW
EXECUTE FUNCTION identify_clients();

trigger to track changes in the auto table

CREATE OR REPLACE FUNCTION track_auto_changes()
RETURNS TRIGGER AS $$
BEGIN
    IF TG_OP = 'UPDATE' THEN
        INSERT INTO auto_history (brand_id, brand_auto, count, model, price, modification_time)
        VALUES (OLD.brand_id, OLD.brand_auto, OLD.count, OLD.model, OLD.price, NOW());
    END IF;
    RETURN NEW;
END;
$$ LANGUAGE plpgsql;

CREATE TRIGGER track_auto_changes_trigger
AFTER UPDATE
ON auto
FOR EACH ROW
EXECUTE FUNCTION track_auto_changes();




