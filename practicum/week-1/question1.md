1. Download and install PostgreSQL database (it is available at https://www.postgresql.org)
2. Create a database and name it as ISTA495.practicum
3. Ctreat the following table:
  - table name: world
  - table columns: id, country, population, area, migrants,fertility,medianage,urbanpopulation(id is a number, everything else is a string).
4. Populate the world table using the csv file included in this folder

Hint:

* [How to import CSV file into PostgreSQL table](https://www.postgresqltutorial.com/import-csv-file-into-posgresql-table/)

* [How to import a selected number of the columns of a csv file](https://stackoverflow.com/questions/12618232/copy-a-few-of-the-columns-of-a-csv-file-into-a-table/49906327)


Step 1 Create Database:

-- Database: ISTA495.practicum

-- DROP DATABASE "ISTA495.practicum";

CREATE DATABASE "ISTA495.practicum"
    WITH
    OWNER = postgres
    ENCODING = 'UTF8'
    LC_COLLATE = 'C'
    LC_CTYPE = 'C'
    TABLESPACE = pg_default
    CONNECTION LIMIT = -1;



Step 2 Create Table:

My query:

CREATE TABLE world (
    id INTEGER,
    country VARCHAR(50),
    population VARCHAR(50),
    area VARCHAR(50),
    migrants VARCHAR(50),
    fertility VARCHAR(50),
    medianage VARCHAR(50),
    urbanpopulation VARCHAR(50),
    PRIMARY KEY (id)
)

SQL result:

-- Table: public.world

-- DROP TABLE public.world;

CREATE TABLE public.world
(
    id integer NOT NULL,
    country character varying(50) COLLATE pg_catalog."default",
    population character varying(50) COLLATE pg_catalog."default",
    area character varying(50) COLLATE pg_catalog."default",
    migrants character varying(50) COLLATE pg_catalog."default",
    fertility character varying(50) COLLATE pg_catalog."default",
    medianage character varying(50) COLLATE pg_catalog."default",
    urbanpopulation character varying(50) COLLATE pg_catalog."default",
    CONSTRAINT world_pkey PRIMARY KEY (id)
)

TABLESPACE pg_default;

ALTER TABLE public.world
    OWNER to postgres;

Messages:
CREATE TABLE

Query returned successfully in 100msec.



Step 3 Populate table with csv file:


First we create a temp table to transfer the data into

CREATE TABLE tempworld (
    id INTEGER,
    country VARCHAR(50),
    population VARCHAR(50),
    yearlychange VARCHAR(50),
    netchange VARCHAR(50),
    area VARCHAR(50),
    migrants VARCHAR(50),
    fertility VARCHAR(50),
    medianage VARCHAR(50),
    urbanpopulation VARCHAR(50),
    PRIMARY KEY (id)
)

SQL result:

-- Table: public.tempworld

-- DROP TABLE public.tempworld;

CREATE TABLE public.tempworld
(
    id integer NOT NULL,
    country character varying(50) COLLATE pg_catalog."default",
    population character varying(50) COLLATE pg_catalog."default",
    yearlychange character varying(50) COLLATE pg_catalog."default",
    netchange character varying(50) COLLATE pg_catalog."default",
    area character varying(50) COLLATE pg_catalog."default",
    migrants character varying(50) COLLATE pg_catalog."default",
    fertility character varying(50) COLLATE pg_catalog."default",
    medianage character varying(50) COLLATE pg_catalog."default",
    urbanpopulation character varying(50) COLLATE pg_catalog."default",
    CONSTRAINT tempworld_pkey PRIMARY KEY (id)
)

TABLESPACE pg_default;

ALTER TABLE public.tempworld
    OWNER to postgres;


Next we import the csv file into this table by right clicking our
table and importing it via pgAdmin.

Finally we copy the rows we want from tempworld into our world table
and drop tempworld.

insert into world (id, country, population, area, migrants,fertility,medianage,urbanpopulation)
select id, country, population, area, migrants,fertility,medianage,urbanpopulation
from tempworld

drop table tempworld

![p1](/Users/petervukasin/Desktop/ISTA495/ISTA495/practicum/week-1/images/p1.png)