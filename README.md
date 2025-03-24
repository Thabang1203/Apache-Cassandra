# Apache-Cassandra
CQL ASSESSMENT 20/03/2025

1.	Create a keyspace:

create keyspace EcommerceCatalog with replication = {'class': 'SimpleStrategy', 'replication_factor': 1};

2.	Use the Keyspace:

 use EcommerceCatalog;

3.	Create the Categories Table:

create table categories(
                    ... category_id UUID primary key,
                    ... category_name text,
                    ... description text);
	       … select * from categories;

4.	Create the Brands Table:

create table brands(
                    ... brand_id uuid primary key,
                    ... brand_name text,
                    ... country_of_origin text);
	       … select * from brands;

5.	Create the Product Table:

create table products(
                    ... product_id uuid primary key,
                    ... product_name text,
                    ... category_id uuid,
                    ... brand_id uuid,
                    ... price decimal,
                    ... inventory_count int,
                    ... description text);

6.	Insert Records into Categories Table:

insert into categories(category_id,category_name,description) values (uuid(),'Electronics','Electronic devices');
insert into categories(category_id,category_name,description) values (uuid(),'Computers','Laptops and desktops');
insert into categories(category_id,category_name,description) values (uuid(),'Smartphones','Mobile phones');
insert into categories(category_id,category_name,description) values (uuid(),'Clothing','Apparel');
insert into categories(category_id,category_name,description) values (uuid(),'Menswear','Chlothing for men');
insert into categories(category_id,category_name,description) values (uuid(),'Womenswear','Chlothing for women');
select * from categories;

7.	Insert Records into Brands Table:

insert into brands(brand_id,brand_name,country_of_origin) values(uuid(),'TechCorp','USA');
insert into brands(brand_id,brand_name,country_of_origin) values(uuid(),'StyleGen','Italy');
insert into brands(brand_id,brand_name,country_of_origin) values(uuid(),'MobilePro','China');
insert into brands(brand_id,brand_name,country_of_origin) values(uuid(),'FashionFit','UK');
insert into brands(brand_id,brand_name,country_of_origin) values(uuid(),'ElectroMax','Japan');
insert into brands(brand_id,brand_name,country_of_origin) values(uuid(),'HomeStyle','Canada');
select * from brands;

8.	Insert Records into Products Table:

insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values(uuid(),'Laptop X
100',53fb1e3a-b225-4bd2-a0f7-17482076b4a2,d8e2f19e-c84b-4284-9781-96589704bc65,1200.00,50,'High-performance laptop');
insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values(uuid(),'Smartphone Z5',cf42660b-4089-4f30-bf0e-11a0740567cd,8a7531bf-2e87-4514-9772-84f740a7b4f2,800.00,100,'Latest smartphones');
insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values (uuid(), 'Mens S
hirt', 031e24e0-a59a-4de0-b7d6-b8491a5deb30, d9cfeccc-ed87-4155-8b24-5967ed80f8e9,50.00,150,'Classic shirt');
insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values (uuid(), 'Womens Dress',3a3c2361-fc3a-440a-9738-3b5583aa520b,8f26fb5b-e286-4d88-b7ed-38dc85f15adf,120.00,110,'Elegant dress');
insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values (uuid(), 'Desktop Pro 2000',53fb1e3a-b225-4bd2-a0f7-17482076b4a2,406525f8-61cf-4a84-a098-902df043f5e1,1500.00,30,'Powerful desktop');
insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values (uuid(), 'Smartphone Lite',cf42660b-4089-4f30-bf0e-11a0740567cd,8a7531bf-2e87-4514-9772-84f740a7b4f2,300.00,200,'Budget phone');
insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values (uuid(), 'Mens Pants',031e24e0-a59a-4de0-b7d6-b8491a5deb30,8f26fb5b-e286-4d88-b7ed-38dc85f15adf,75.00,120,'Comfortable pants');
insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values (uuid(), 'Womens Blouse',8f26fb5b-e286-4d88-b7ed-38dc85f15adf,d9cfeccc-ed87-4155-8b24-5967ed80f8e9,80.00,130,'Stylish blouse');
insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values (uuid(), 'Laptop Mini',53fb1e3a-b225-4bd2-a0f7-17482076b4a2,d8e2f19e-c84b-4284-9781-96589704bc65,700.00,80,'Portable laptop');
insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values (uuid(), 'Smartphone Pro',cf42660b-4089-4f30-bf0e-11a0740567cd,406525f8-61cf-4a84-a098-902df043f5e1,1100.00,60,'Professional phone');
insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values (uuid(),'Mens jacket',031e24e0-a59a-4de0-b7d6-b8491a5deb30,d8e2f19e-c84b-4284-9781-96589704bc65,150.00,90,'Warm Jacket');
insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values (uuid(),'Womens skirt',3a3c2361-fc3a-440a-9738-3b5583aa520b,8f26fb5b-e286-4d88-b7ed-38dc85f15adf,60.00,190,'Casual skirt');
insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values (uuid(),'Tablet Pro',53fb1e3a-b225-4bd2-a0f7-17482076b4a2,406525f8-61cf-4a84-a098-902df043f5e1,900.00,70,'Professional tablet');
insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values (uuid(),'Headphones Wireless',c23b384c-b086-4720-9041-e0a3926f7531,8a7531bf-2e87-4514-9772-84f740a7b4f2,180.00,160,'High quality headphones');
insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values (uuid(),'Smart TV',8a7531bf-2e87-4514-9772-84f740a7b4f2,653b3b28-fbba-4965-ab1f-1c5c109ea221,600.00,400,'Smart television');
select * from products;

9.	Batch Insert Records:

begin batch 
 insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values(uuid(),'Sport T-Shirt',031e24e0-a59a-4de0-b7d6-b8491a5deb30,8f26fb5b-e286-4d88-b7ed-38dc85f15adf,40.00,250,'Sporty T-shirt');
 insert into products(product_id,product_name,category_id,brand_id,price,inventory_count,description) values(uuid(),'Portable SSD',8f26fb5b-e286-4d88-b7ed-38dc85f15adf, d8e2f19e-c84b-4284-9781-96589704bc65,120.00,140,'Fast portable storage'); 
 update products set price = 1250.00 where product_id = 3d9dd865-9dd5-4614-bb48-911889da468f; 
delete from products where product_id = 84424be9-7c3b-4215-b983-86a6df7b19df;
 apply batch;
select * from products;

10.	Update a Record:

update products set description = 'Premium classic shirt' where product_id = 7f7d668f-4710-4d71-927b-7d6ffd58d219;

11.	Delete a Record:

delete from brands where brand_id =  653b3b28-fbba-4965-ab1f-1c5c109ea221;

12.	Create an Index:

create INDEX cateid_idx on products (category_id);


13.	Query the Products Table:

select * from products where price > 500.00 allow filtering;

14.	Retrieve Products by Brand:

select * from Products where brand_id=  d8e2f19e-c84b-4284-9781-96589704bc65 allow filtering;

15.	Calculate the Average Price:

select avg(price) from products where category_id = uuid() allow filtering;

16.	Find the Minimum Inventory Count:

SELECT MIN(inventory_count) FROM products where product_id = uuid() allow filtering;

17.	Find the Maximum Inventory Count:

SELECT MAX(inventory_count) FROM products where product_id = uuid() allow filtering;

18.	Count Products in a Category:

Select count(category_id) from products where category_id = uuid();

19.	Count Brands from a Country

select count (*) from Brands where brand_id=406525f8-61cf-4a84-a098-902df043f5e1;

