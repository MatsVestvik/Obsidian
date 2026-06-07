Normal Form kommer i ulike grader.

| Form | Forklaring |
|-------|------------|
| UNF | En tabell er på unormalisert form dersom den inneholder repeterende grupper eller flerverdiattributter . Dette betyr at én rute i tabellen kan inneholde en liste med verdier i stedet for én enkel verdi |
| 1NF | En relasjon er på 1NF hvis alle attributtene inneholder kun atomære verdier |
| 2NF | __Krav__: Relasjonen må være på 1NF og skal ikke inneholde partielle avhengigheter . __Definisjon__: En partiell avhengighet oppstår når et ikke-nøkkel-attributt er funksjonelt avhengig av bare en del av en sammensatt primærnøkkel . __Viktig__: 2NF er kun relevant for tabeller med sammensatt primærnøkkel; en tabell med en enkel primærnøkkel er automatisk på 2NF dersom den er på 1NF
| 3NF | __Krav__: Relasjonen må være på 2NF og skal ikke inneholde transitive avhengigheter . __Definisjon__: En transitiv avhengighet betyr at verdien til et ikke-nøkkel-attributt bestemmes av verdien til et annet ikke-nøkkel-attributt . __Huskeregel__: En vanlig formulering er at "alle attributter må utgå fra primærnøkkelen" .
| BCNF | __Krav__: En relasjon er på BCNF dersom den er på 3NF og enhver determinant er en kandidatnøkkel . Forhold til 3NF: Hvis en tabell bare har én kandidatnøkkel, er 3NF og BCNF i praksis det samme . BCNF er en strengere form som håndterer tilfeller der det finnes overlappende kandidatnøkler

For å forklare det enkel er UNF ikke normal form. Den er UNF dersom den ikke møter kravene til 1NF.

>[!UNF]
>
>|Elev | Fag |
>|-----|------|
>| Mats | matte, engelsk |
>| Birgitte | programering, tysk |

1NF betyr at ingen kolonne i tabellen kan inneholde en liste. f.eks:

>[!1NF]
>
>| Elev | Fag |
>|------|-----|
>|Mats | Matte |
>|Mats | engelsk|
>|Birgitte | programmering |
>|Birgitte | tysk |

For 2NF gjelder kun dette prinsippet på tabeller med sammensatt primær nøkkel. 

|studentid_fag| studentid | fag | lærer | lærer kontor |
|-------------| -----------|-----|---------|------------|
|1_matte|1| matte |tore | a112 |

Hvis vi betrakter tabellen over med en sammensatt primærnøkkel. Vi kan se at lærer er kun avhengig av fag ikke student_id.  Dette kalles en delvis avhengighet og er ikke tilatt under 2 NF prinsippet.

3NF krever at de tidligere kravene. Det skal heller ikke eksisteer transistive avhengigheter. Et ikke nøkkelattribut skal ikke være avhenging av et annet ikke nøkkel attribut

| ansatt_id | navn | avdeling | avdelingsjef |
|-----------|-----|---------|------------|
|1| mats | it | birgitte |
|2| saga | fun | birgitte |

Vi kan betrakte eksempel tabellen over. Vi ser at avdelingsjef er kun avhengig av avdeling, som ikke er en nøkkelverdi. Dette er en transistiv avhengighet og er ikke tilatt. Løsningen hadde vært å lage en ny tabell som representerer avdeling.

BCNF sier at alle determinanter må være supernøkler