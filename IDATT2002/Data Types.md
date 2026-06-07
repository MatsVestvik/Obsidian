| type | forklaring | brukseksempel |
|------|------------|------------------|
| int | tall fra -100000 til 100000 | telefonnummer |
| smallint | -32768 til 32767 | |
| tinyint | 0 til 255 | |
| bigint | 9223372036854775807 | |
| decimal(p,s) | p defines total number of digits, s defins digits after decimal | decimal(3,2) 3.14 |
| float | tilnærming av desivmal tall for mer effektiv lagring | |
| real | nøyaktig float tall | |
| char(n) | lagrer nøyaktig n characterer | char(2) tilatter for eksempel landskoder US, NO|
| varchar(n) lagrer opp til n karakterer | varchar(2) lagrer for eksempel U, UN |
| text | lagrer lange string verdier som et dokument eller en json fil | |
| date | lagrer datoen | |
| time | lagrer tiden | |
| datetime | lagerer dato og tid | |
| timestamp | lagrer dato og tid nå | |
| interval | lagrer en lengde av tid | |
| binary() | | |
| varbinary() | | |
| blob | binary large object | |
| boolean| | |
| enum() | tilatter kun verdier lagret i enum(v,v,v) | enum(test, ikke test, 2) kan lagre disse verdiene |
| json | | |
| xml | | |