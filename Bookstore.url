drop database bookstore;
CREATE database bookstore;

use bookstore;

drop table if exists Books;
drop table if exists Authors;
drop table if exists Inventory;
drop table if exists OrderItem;
drop table if exists ShoppingCart;
drop table if exists Customer;

create table Authors (
	authorId varchar(10),
    firstName varchar(10),
    mi char(1),
    lastName varchar(10),
    primary key (authorID)
);

create table Books (
	isbn varchar(13), 
	authorID varchar(25), 
	title varchar(30), 
	genre varchar(10),  
	releaseDate date, 
	price double,
	primary key (isbn),
	foreign key (authorID) references Authors(authorID)
);

create table Inventory (
	isbn varchar(13),
    stockUsed integer,
    stockAvailible integer,
    foreign key (isbn) references Books(isbn)
);

create table OrderItem (
	orderID varchar(10),
    isbn varchar(13),
    amount integer,
    price double,
    primary key (orderID),
    foreign key (isbn) references Books(isbn)
);

create table Customer (
	username varchar(10),
    firstName varchar(10), 
    lastName varchar(10),
    primary key (username)
);

create table ShoppingCart (
	cartID integer,
    username varchar(10),
    orderDate date,
    totalCost double,
    primary key (cartID),
    foreign key (username) references Customer(username)
);

insert into Authors values (
	'001', 'Christie', null, 'Golden'
);

insert into Authors values (
	'002', 'David', null, 'Levithan'
);

insert into Authors values (
	'003', 'Nicholas', null, 'Sparks'
);

insert into Books values (
	'9780399594090', '001', 'WoW: Before the Storm', 'Fantasy', '2018-06-12', 28.00
);

insert into Books values (
	'9781416550860', '001', 'WoW: Beyond the Dark Portal', 'Fantasy', '2008-06-24', 7.99
);

insert into Books values (
	'9780989700139', '001', 'WoW: Rise of the Horde', 'Fantasy', '2006-12-01', 14.95
);

insert into Books values (
	'9780307931894', '002', 'Every Day', 'Romance', '2012-08-28', 7.99
);

insert into Books values (
	'9780399553059', '002', 'Someday', 'Romance', '2018-10-02', 12.91
);

insert into Books values (
	'9780385756235', '002', 'Another Day', 'Romance', '2015-07-30', 9.99
);

insert into Books values (
	'9780446547635', '003', 'The Best of Me', 'Romance', '2011-10-01', 3.50
);	

insert into Inventory values (
	'9780399594090', 4000, 6000
);

insert into Inventory values (
	'9781416550860', 1500, 6000
);

insert into Inventory values (
	'9780989700139', 3020, 6000
);

insert into Inventory values (
	'9780307931894', 3200, 4000
);

insert into Inventory values (
	'9780399553059', 2203, 4000
);

insert into Inventory values (
	'9780385756235', 1248, 4000
);

insert into Inventory values (
	'9780446547635', 1426, 4000
);

