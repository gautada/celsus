# celsus

This project is an architecture library

Celsus - This project was named after the [Library of Celsus](https://www.history.com/news/8-impressive-ancient-libraries) - There were over two-dozen major libraries in the city of Rome during the imperial era, but the capital wasn’t the only place that housed dazzling collections of literature. Sometime around 120 A.D., the son of the Roman consul Tiberius Julius Celsus Polemaeanus completed a memorial library to his father in the city of Ephesus (modern day Turkey). The building’s ornate façade still stands today and features a marble stairway and columns as well as four statues representing Wisdom, Virtue, Intelligence and Knowledge. Its interior, meanwhile, consisted of a rectangular chamber and a series of small niches containing bookcases. The library may have held some 12,000 scrolls, but it most striking feature was no doubt Celsus himself, who was buried inside in an ornamental sarcophagus.

This project provides a framework and a library for solution architecture.

## Modeling

- [PlantUML](https://plantuml.com)
- [
https://plantuml-stdlib.github.io/C4-PlantUML/

https://aws.amazon.com/architecture/icons/
https://learn.microsoft.com/en-us/azure/architecture/icons/

## SQL

CREATE TABLE containers (

);



CREATE DATABASE architecture;

DROP TABLE IF EXISTS node_tag_map;
DROP TABLE IF EXISTS tags;
DROP TABLE IF EXISTS nodes;

CREATE TABLE tags (
 tag VARCHAR(50) PRIMARY KEY NOT NULL
);

CREATE TABLE nodes (
 alias VARCHAR(25) PRIMARY KEY NOT NULL,
 label VARCHAR(255) NOT NULL,
 type VARCHAR(255),
 description TEXT,
 sprite VARCHAR(255),
 link VARCHAR(255)
);

CREATE TABLE node_tag_map (
 node VARCHAR(25) NOT NULL,
 tag VARCHAR(50) NOT NULL,
 PRIMARY KEY (node, tag)
);

CREATE TABLE systems (
 alias VARCHAR(25) PRIMARY KEY NOT NULL,
 label VARCHAR(255) NOT NULL,
 type VARCHAR(25) NOT NULL,
 external BOOLEAN NOT NULL,
 description TEXT,
 sprite VARCHAR(255),
 link VARCHAR(255),
 role VARCHAR(25)
);

CREATE TABLE system_tag_map (
 system VARCHAR(25) NOT NULL,
 tag VARCHAR(50) NOT NULL,
 PRIMARY KEY (node, tag)
);

-- Physical Locations
INSERT INTO nodes VALUES ('HOME', 'Home', 'Location', 'This is a standard home location, i.e. a provate residence outside of a managed enterprise environment', NULL, NULL, NULL);

-- Profiles are virtual profiles for the network
