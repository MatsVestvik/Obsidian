Kan hjelpe med å gjøre søk raskere. Med en index som:
CREATE INDEX ansatt_etternavn ON ansatt(etternavn);

SELECT * FROM ansatt WHERE etternavn = 'nilsen';

