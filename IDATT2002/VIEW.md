Vi kan se hvordan en view kan være nyttig hvis vi betrakter eksempelet under hvor view kan skjule data.
```
CREATE TABLE ansatt( 
	ansattid int primary key,
	navn varchar(255),
	lønn int
);
```

```
CREATE VIEW ansattView AS
SELECT
	ansattid,
	navn
from ansatt
; 
```

Det kan også være nyttig å lage en view som representerer en select spørring som blir gjort ofte.
Her kan du bruke join settninger for å sette sammen tabeller.

```
CREATE VIEW bestilling_kunde AS
SELECT 
	kunde.navn,
	orde.levdato
FROM ordre
JOIN kunde ON  ordre.kundeid = kunde.id;

```