# celsus

This project is an architecture library

Celsus - This project was named after the [Library of Celsus](https://www.history.com/news/8-impressive-ancient-libraries) - There were over two-dozen major libraries in the city of Rome during the imperial era, but the capital wasn’t the only place that housed dazzling collections of literature. Sometime around 120 A.D., the son of the Roman consul Tiberius Julius Celsus Polemaeanus completed a memorial library to his father in the city of Ephesus (modern day Turkey). The building’s ornate façade still stands today and features a marble stairway and columns as well as four statues representing Wisdom, Virtue, Intelligence and Knowledge. Its interior, meanwhile, consisted of a rectangular chamber and a series of small niches containing bookcases. The library may have held some 12,000 scrolls, but it most striking feature was no doubt Celsus himself, who was buried inside in an ornamental sarcophagus.

![Context Diagram - Solution Architecture](https://puml.gautier.org/plantuml/png/jLPDR-Cs4BthLymQ1Me3jdF9QL4qS6nd6s2tCPnsUrWi35eQsSHAf4fIcmYk_tk7r1TfnoxGehbOecRcFRutG-OT5t5M9WW_pMzlvhVJeiopdwDtuUfcBeN1LtFbA-C2rSNlUI45YalvYqgmdCUNlcAHoIhlqwCVeU53JvFwZvuEpvKscF-rf4-gK5pZvdWlIv4mLGrPnfaUGyQsc8tXS6Ug0ezZk3DiHyi_P5ny6r6D5IejnM6pV3N7avox17Miw5TJROFdkJNylybjDkGaxBVaDjMjdrOq6E_5FxDo9HhrpqetwqtfwNHQ9wmnOuPBeVUyy7FgDFewD78CgPBv61nydVPbVWkhZ0dp-wUFNuTxOmhz_kQci2jasqIR9EFRwOwRVRcTSadMJjhm6zB0S9CX31fdOS7PJh4S9j3x2JCLxscNiIaL3gAeTiiAFXnGpaRdE1Z3WDvH2PR1yhL0PUpIJ02sgxHZRYemUsPWppGKvJRZUey9CDfEoWMtcmUf82ODZ2Bv3R145eP2jZOHROsMqn1VMLva-9wKsPMad2GxFgD8xE-pORR_4WttCgb6Wr5KTqdFcPLcBycwAc0-yrTzyfOIJr0vWo0baguHU5nlh2MbPLOw2y_fsTKntACsi58iDZpcI0k-jF10okEBLDyynjqe3NeSnxb_6y4X0jyKWootCO-MWPtWclPlpVAN3qgMnLV22B98x-jMSl5_MtbVQXewhU7fXMPl3FF79oi5-EvPce5xZ-A2UotVhAfP4VX_yF6X5EIQnLdZdoLNJbXjUusguQxoYVQcCVAtdPp0jN2ed8MD6-GqknJhx5lB39rxNO9s2SyDQo_S1jMSY4eWJ_02YOnBkn_IxDGTvdSe7IMAzbLRdxD2zoFIbVTQG8EHOG7NEjJv0JC24Z4dbIsPbV_YCNEGcbePDRLPeJ15XI96vo83mzGEcm2GfOabjN80menbwY3wnrC0Tx3ohSKGmBQsUMDI9HmacJe6BKyVfQDbYw_zboj8jYrZXKJyJQ2QBRpG4Gwwm9YdFAxxLcPoTofcsxj-Hrp73wMpa1tAjXt8O59IDmfKriTDA4KtM0llULONze7jB5g14r18TByx3JfC4YFDEAbkDqpzoBfn39MMBA4ET3hJu-HJ_JoZ7gKpbhRHmMeVry6MeW5Ehg3PtgNUocb9AZepADZm73DRXCgx2dNWyCMDGqcuMuIkTCgLDkvOE4R7AB8tk7zVdbr3AoM_q-5axNInmSUpQBlV9j0xkSzEnwj5pwAzei5GXcU7FScxi7wMWeo5KxkD2iR2Irc-8dKyJwisqE_Ue5vtbxqPsLUy6XVGE8lqEzZFciKnzXls-iuFMjUkluKQYFUP_kjBxA0T7fefQcwKva8vlbMXlT3dxNNQ1R5J7g7kzKroubvEfpFDa0g30hKl1dadvuMGGECWA7h-vUcFpSVbX-MlY-7eRm00)



This project provides a framework and a library for solution architecture.


https://www.sqlite.org/index.html
https://github.com/coleifer/sqlite-web




## Modeling
https://github.com/plantuml-stdlib

- 
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

## Diagramming

- https://c4model.com
- [PlantUML](https://plantuml.com)
 - [Standard Library](https://github.com/plantuml/plantuml-stdlib) [[Unofficial](https://github.com/plantuml-stdlib)]
