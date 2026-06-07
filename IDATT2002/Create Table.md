>[!example]
> Hvis vi vil lage en relasjon brukere lager vi og definerer attributtene våre i samme querry.
> ```
>CREATE TABLE brukere (
> 	id INT AUTO_INCREMENT PRIMARY KEY,
> 	navn VARCHAR(100) NOT NULL,
> 	epost VARCHAR(150) NOT NULL UNIQUE,
> 	alder INT,
> 	opprettet_dato TIMESTAMP DEFAULT CURRENT_TIMESTAMP
> 	FOREIGN KEY (epost) REFERENCES anotertable(colomn)
>);
>```
>Vi velger id som en primary key. Det vil si at den må være unik, ingen rader kan ha lik id verdi.
>Vi gir den også  AUTO_INCREMENT attributtet. Dette gjør at denne verdien er automatisk generert for hver nye tuppel. Første raden blir 1, andre blir 2 også videre. 

