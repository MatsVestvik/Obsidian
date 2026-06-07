| command | forklaring | eksempel |
|------------|------------|------------|
| ADD | brukes for å legge til en kolonne til en eksisterende tabell | alter table ntnu add ant_studenter int;
| DROP | brukes for å fjerne ting for eksempel en kolonne | alter table ntnu drop ant_studenter |
| MODIFY | brukes til å endre datatype i en kolonne | alter table ntnu modify ant_studenter varchar(255) |
| RENAME | bruker til å gi nytt navn til en kolonne | alter table ntnu rename ant_studenter to name |
| ADD PRIMARY KEY | brukes for å legge til en primary key | alter table ntnu add primary key(name) |
| ADD FOREIGN KEY | brukes for å legge til en foreign key | alter table ntny add foreign key(stud_id) references student(id) |

>[!generell syntax]
>ALTER TABLE tablename __COMMAND__ kolonnenavn