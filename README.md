# Opdracht 1: The Lab

- a) Maak een database genaamd the_lab
- b) Neem de volgende code over en voer deze queries uit!

```sql
create table Scientists (
  SSN int,
  Name Char(30) not null,
  Primary Key (SSN)
);

Create table Projects (
  Code Char(4),
  Name Char(50) not null,
  Hours int,
  Primary Key (Code)
);

create table AssignedTo (
  Scientist int not null,
  Project char(4) not null,
  Primary Key (Scientist, Project),
  Foreign Key (Scientist) references Scientists (SSN),
  Foreign Key (Project) references Projects (Code)
);
```

c) Neem de volgende code over en voer deze queries uit!

```sql
INSERT INTO Scientists(SSN,Name)
  VALUES(123234877,'Michael Rogers'),
    (152934485,'Anand Manikutty'),
    (222364883, 'Carol Smith'),
    (326587417,'Joe Stevens'),
    (332154719,'Mary-Anne Foster'),
    (332569843,'George ODonnell'),
    (546523478,'John Doe'),
    (631231482,'David Smith'),
    (654873219,'Zacary Efron'),
    (745685214,'Eric Goldsmith'),
    (845657245,'Elizabeth Doe'),
    (845657246,'Kumar Swamy');

 INSERT INTO Projects ( Code,Name,Hours)
 VALUES ('AeH1','Winds: Studying Bernoullis Principle', 156),
       ('AeH2','Aerodynamics and Bridge Design',189),
       ('AeH3','Aerodynamics and Gas Mileage', 256),
       ('AeH4','Aerodynamics and Ice Hockey', 789),
       ('AeH5','Aerodynamics of a Football', 98),
       ('AeH6','Aerodynamics of Air Hockey',89),
       ('Ast1','A Matter of Time',112),
       ('Ast2','A Puzzling Parallax', 299),
       ('Ast3','Build Your Own Telescope', 6546),
       ('Bte1','Juicy: Extracting Apple Juice with Pectinase', 321),
       ('Bte2','A Magnetic Primer Designer', 9684),
       ('Bte3','Bacterial Transformation Efficiency', 321),
       ('Che1','A Silver-Cleaning Battery', 545),
       ('Che2','A Soluble Separation Solution', 778);

 INSERT INTO AssignedTo ( Scientist, Project)
   VALUES (123234877,'AeH1'),
    (152934485,'AeH3'),
    (222364883,'Ast3'),
    (326587417,'Ast3'),
    (332154719,'Bte1'),
    (546523478,'Che1'),
    (631231482,'Ast3'),
    (654873219,'Che1'),
    (745685214,'AeH3'),
    (845657245,'Ast1'),
    (845657246,'Ast2'),
    (332569843,'AeH4');
```

## Uit te voeren opdracht

Probeer dan de volgende opdracht uit te voeren: Maak een lijst van alle namen van de wetenschappers, de namen van hun projecten en de uren die die wetenschapper aan elk project heeft gewerkt, in alfabetische volgorde van projectnaam en vervolgens naam van de wetenschapper.

# Opdracht 2: Bioscopen en films

1. Maak een database genaamd movies_challenge.
2. Maak een database aan de hand van de gegevens onderaan
3. Beantwoord onderstaande vragen:
   • Selecteer alle titels van de films
   • Toon alle ratings 1 keer
   • Toon de films zonder rating
   • Toon de bioscopen waar geen film draait
   • Toon alle data van de bioscopen met daarbij de informatie van de film die getoond wordt.
   • Toon alle data van de films en als de film in een bioscoop draait dan toon je die info
   • Toon de titels van films die niet in de bioscoop draaien
   • Verander de rating van alle films zonder rating in "G"
   • Verwijder bioscopen die films tonen met rating "NC-17".

```sql
   INSERT INTO Movies(Code,Title,Rating) VALUES(9,'Citizen King','G');
   INSERT INTO Movies(Code,Title,Rating) VALUES(1,'Citizen Kane','PG');
   INSERT INTO Movies(Code,Title,Rating) VALUES(2,'Singin'' in the Rain','G');
   INSERT INTO Movies(Code,Title,Rating) VALUES(3,'The Wizard of Oz','G');
   INSERT INTO Movies(Code,Title,Rating) VALUES(4,'The Quiet Man',NULL);
   INSERT INTO Movies(Code,Title,Rating) VALUES(5,'North by Northwest',NULL);
   INSERT INTO Movies(Code,Title,Rating) VALUES(6,'The Last Tango in Paris','NC-17');
   INSERT INTO Movies(Code,Title,Rating) VALUES(7,'Some Like it Hot','PG-13');
   INSERT INTO Movies(Code,Title,Rating) VALUES(8,'A Night at the Opera',NULL);

INSERT INTO MovieTheaters(Code,Name,Movie) VALUES(1,'Odeon',5);
INSERT INTO MovieTheaters(Code,Name,Movie) VALUES(2,'Imperial',1);
INSERT INTO MovieTheaters(Code,Name,Movie) VALUES(3,'Majestic',NULL);
INSERT INTO MovieTheaters(Code,Name,Movie) VALUES(4,'Royale',6);
INSERT INTO MovieTheaters(Code,Name,Movie) VALUES(5,'Paraiso',3);
INSERT INTO MovieTheaters(Code,Name,Movie) VALUES(6,'Nickelodeon',NULL);
```
