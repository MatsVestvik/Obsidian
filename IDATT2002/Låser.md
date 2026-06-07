Lås en tabell for å forhindre endringer

Granularitet beskriver hvor stor del av databasen som lagres (en verdi, rad, tabell, databasen).

### Delt lås
Brukes kun til leseing og tillater flere operasjoner å lese samme data, men forhindrer dem fra å gjøre endringer

### Eksklusiv lås
En eksklusiv lås forutsetter at objektet ikke er låst av noen andre. Den gjør det kun mulig for transaksjonen som lagde låsen og lese og skrive til objektet.

### To fase låsing og vranglås
