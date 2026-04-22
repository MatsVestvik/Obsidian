## Hva er en Hamiltonsk graf?

En **Hamiltonsk graf** er en graf som inneholder en **Hamilton-syklus** (en syklus som besøker **hver node** nøyaktig én gang og returnerer til startpunktet).

## De viktigste definisjonene

| Begrep | Definisjon |
|--------|------------|
| **Hamilton-sti** | En sti som besøker **hver node** nøyaktig én gang (starter og slutter i ulike noder) |
| **Hamilton-syklus** | En Hamilton-sti som **starter og slutter i samme node** |
| **Hamiltonsk graf** | En graf som har en Hamilton-syklus |

## Forskjellen mellom Euler og Hamilton

| | **Euler** | **Hamilton** |
|---|-----------|--------------|
| **Besøker** | Hver **kant** én gang | Hver **node** én gang |
| **Fokus** | Kanter | Noder |
| **Enkel å sjekke?** | Ja (Eulers teorem) | Nei (NP-fullstendig) |
| **Kriterium** | Gradene til nodene | Ingen enkel regel |
