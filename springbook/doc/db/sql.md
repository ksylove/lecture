CREATE DATABASE testMysql default CHARACTER SET UTF8;

show databases;

CREATE USER 'testUser'@'localhost' IDENTIFIED BY '1234';
CREATE USER 'testUser'@'172.17.0.1' IDENTIFIED BY '1234';

GRANT ALL PRIVILEGES ON testMysql.* TO 'testUser'@'localhost';
GRANT ALL PRIVILEGES ON testMysql.* TO 'testUser'@'172.17.0.1';

FLUSH PRIVILEGES;

CREATE table users (
id varchar(10) primary key,
name varchar(20) not null,
password varchar(10) not null
);