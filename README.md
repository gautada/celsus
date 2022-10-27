# celsus

This project is an architecture library

Celsus - This project was named after the [Library of Celsus](https://www.history.com/news/8-impressive-ancient-libraries) - There were over two-dozen major libraries in the city of Rome during the imperial era, but the capital wasn’t the only place that housed dazzling collections of literature. Sometime around 120 A.D., the son of the Roman consul Tiberius Julius Celsus Polemaeanus completed a memorial library to his father in the city of Ephesus (modern day Turkey). The building’s ornate façade still stands today and features a marble stairway and columns as well as four statues representing Wisdom, Virtue, Intelligence and Knowledge. Its interior, meanwhile, consisted of a rectangular chamber and a series of small niches containing bookcases. The library may have held some 12,000 scrolls, but it most striking feature was no doubt Celsus himself, who was buried inside in an ornamental sarcophagus.

This project provides a framework and a library for solution architecture.


https://www.sqlite.org/index.html
https://github.com/coleifer/sqlite-web


## Modeling
https://github.com/plantuml-stdlib

- [PlantUML](https://plantuml.com)
- [
https://plantuml-stdlib.github.io/C4-PlantUML/

https://aws.amazon.com/architecture/icons/
https://learn.microsoft.com/en-us/azure/architecture/icons/

## SQL

' Context Diagram
' {Enterprise|System_}Boundary(alias, label, ?type, ?tags, $link)
' Person{_Ext}(alias, label, ?descr, ?sprite, ?tags, $link)
' System{Db|Queue}{_Ext}(alias, label, ?descr, ?sprite, ?tags, $link)
' Rel(from, to, label, ?techn, ?descr, ?sprite, ?tags, $link)

CREATE TABLE boundaries (
 alias VARCHAR(25) PRIMARY KEY,
 label VARCHAR(255) NOT NULL,
 type VARCHAR(255) NOT NULL,
 uri VARCHAR(255) NOT NULL
);

CREATE TABLE people (
 alias VARCHAR(25) PRIMARY KEY,
 label VARCHAR(255) NOT NULL,
 external BOOLEAN NOT NULL,
 description TEXT,
 uri VARCHAR(255) NOT NULL
);

CREATE TABLE systems (
 alias VARCHAR(25) PRIMARY KEY,
 external BOOLEAN NOT NULL,
 type VARCHAR(255) NOT NULL,
 label VARCHAR(255) NOT NULL,
 description TEXT,
 uri VARCHAR(255) NOT NULL
);

CREATE TABLE relationships (
 from VARCHAR(25) NOT NULL,
 to VARCHAR(25) NOT NULL,
 label VARCHAR(255),
 technology VARCHAR(25),
 description TEXT,
 uri VARCHAR(255) NOT NULL 
);
