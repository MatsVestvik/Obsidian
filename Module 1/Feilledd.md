### Hva er feilleddet?

Når en funksjon f(x) tilnærmes med et Taylor-polynom av grad n, angir feilleddet (eller restleddet) forskjellen mellom den faktiske verdien av funksjonen og tilnærmingen fra polynomet.

**Notasjon:**
$$
Rn(x)=f(x)−Pn(x)
$$
Her er $P_n(x)$ Taylor-polynomet av grad n utviklet om punktet a.

---

### Lagranges form for restleddet

Den mest brukte formen for å uttrykke feilen er på Lagrange-form:

$$
R_n(x)=\frac{f^{n+1}(c)}{(n+1)!}(x−a)^{n+1}​
$$

**Forklaring av variablene:**

- $f^{n+1}$: Den (n+1)-te deriverte av funksjonen.
    
- c: Et **ukjent** tall som ligger et sted mellom a (sentrum for Taylor-utviklingen) og x (punktet du ønsker å evaluere).
    
- (n+1)!: Faktorialet til n+1, som sørger for at feilen minker raskt når n øker.
    
- $(x−a)^{n+1}$: Avstanden mellom punktet du evaluerer i og sentrum, opphøyd i n+1.
    

### Hva betyr dette i praksis?

- **Proporsjonalitet:** Feilen er proporsjonal med den (n+1)-te deriverte et sted i intervallet mellom a og x.
    
- **Nærhet til sentrum:** Desto nærmere x er a, desto mindre blir faktoren (x−a)n+1, og følgelig blir feilen mindre.
    
- **Estimering av feil:** Siden c er ukjent, kan vi ikke regne ut den eksakte feilen. I stedet brukes formelen til å finne en **øvre grense** for feilen. Dette gjøres ved å finne maksimalverdien til $∣f(n+1)(c)∣$ på intervallet mellom a og x.
    

### Forutsetninger og konsekvenser

1. **Krav til funksjonen:** Formelen forutsetter at f er (n+1) ganger deriverbar på intervallet som inneholder a og x.
    
2. **Økt presisjon med høyere grad:** Når graden n på polynomet øker, vil feilen typisk bli mye mindre fordi vi dividerer med (n+1)!, som vokser eksplosivt.
    
3. **Praktisk bruk:** Hovedformålet med feilleddet er å kunne kvantifisere hvor god tilnærmingen er, for eksempel for å forsikre seg om at feilen er mindre enn en gitt toleranse.