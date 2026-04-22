
## Hva er en eulersk graf?

En **eulersk graf** er en graf som inneholder en **Euler-krets** (en sti som går gjennom hver kant nøyaktig én gang og returnerer til startpunktet).

## De viktigste definisjonene

| Begrep | Definisjon |
|--------|------------|
| **Euler-sti** | En sti som besøker **hver kant** nøyaktig én gang (starter og slutter i ulike noder) |
| **Euler-krets** | En Euler-sti som **starter og slutter i samme node** |
| **Eulersk graf** | En graf som har en Euler-krets |

## Eulers teorem (kjerne-teoremet)

> **Teorem:** En sammenhengende urettet graf har en **Euler-krets** $\iff$ **alle noder har partallsgrad**.

> **Teorem:** En sammenhengende urettet graf har en **Euler-sti** (men ikke krets) $\iff$ nøyaktig **0 eller 2 noder har oddetallsgrad**.

### Rask huskeregel

```mermaid
flowchart TD
    Start[Sammenhengende graf] --> Tell[Tell antall noder med oddetallsgrad]
    
    Tell -->|0 noder| Krets[✅ Euler-krets finnes]
    Tell -->|2 noder| Sti[✅ Euler-sti finnes]
    Tell -->|annet antall| Nei[❌ Ingen Euler-sti/krets]