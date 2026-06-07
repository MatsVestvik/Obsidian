 Select spørringer er en type querry for å hente data ut fra databasen.
 >[!eksempel]
 >SELECT * FROM brukere;
 >
 >Her betyr * alt. Det representerer altså hvilken informasjon du skal hente ut og kan byttes ut med f.eks kolonenavn.
 >brukere representerer hvilken tabell du skal ha det fra


Dette er det enkleste eksempelet hvor vi skriver ut all dataen fra brukere tabellen.

Her er et vanskeliger eksempel
>[!eksempel]
>SELECT DISTINCT stednavn FROM bomstasjon WHERE selskap_navn = 'Tut&Kjør';
>
> Her bruker vi DISTINCT som forteller at vi kun vil ha unike stedsnavn. Det vil si at hvis det for eksempel dukker opp oslo to ganger skriver den det kun en gang. 
> Vi bruker også WHERE som fungerer som en if settning. Vi sier if selskaps_navn er tut og kjør

|begrep|forklaring|plassering
|-----------|----------|------------|
|COUNT(kolonne)|count brukes til å telle hvor mange linjer| Skriver du count(kolonnenavn) får du ut antall rader )|
|AS | Du kan kalle kolonnene du printer ut hva du vil | hvis du skriver et alias bak kolonne navnet skriver du ut kolonnen som alias |
| DISTINCT | skriver du distinct foran en kollene vil du kun skrive ut unike kollone verdier. | Dette kan kombineres med count(dinstinct name) da får du vite hvor mange unike navn som finnes i databasen |
| SUM(kolonne)| summerer alle tallverdier en en kolonne | SUM(age) vil returnere summer av alderene|
| AVG(kolonne) |returnerer gjennomsnittet av en kolonne| AVG(age) vil returnere gjennomsnittsalder|
| MIN(kolonne), MAX(kolonne)|returnerer min og max alder i kolonnen | MIN(kolonne) finner den minste verdien en en kolonne av tallverdier|
| WHERE | her kommer en betingelse| |
| GROUP BY  | Gruperer like verdier | Group by name vil skrive rader med likt navn over og under hverandre for engel navigasjon|
| HAVING | Er etterfulgt av en betingelse | Hvis du for eksempel kun vil skrive ut rader med navnet mats, kan du skrive having name = 'mats'|
| ORDER BY | Er en måte å sortere radene i tabellen og er bruker enten asc desc | hvis du vil sortere etter alder stigene  hadde du skrevet order by age asc |
| IFNULL(vale, value) | hvis en verdi kan være null og du vet dette for eksempel betyr at det er ingen ansatt kan du si det | IFNULL(ansattid, ledig stilling)) |

Som en huskeregel følger en `SELECT`-setning ofte denne rekkefølgen: `SELECT` [kolonner] `FROM` [tabell] `WHERE` [betingelse] `GROUP BY` [gruppering] `HAVING` [betingelse for gruppe] `ORDER BY` [sortering]

