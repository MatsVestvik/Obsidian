## Hva er en sammenhengende graf?
### Definisjon
En **sammenhengende graf** (connected graph) er en graf der det finnes en **sti** mellom **alle** par av noder.
Med andre ord: Du kan komme deg fra hvilken som helst node til hvilken som helst annen node ved å følge kantene i grafen.
### Eksempel 1: Sammenhengende graf
```mermaid
graph LR
    A --- B
    B --- C
    C --- D
    D --- A
    B --- D