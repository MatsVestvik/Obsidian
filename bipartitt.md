## Hva er en bipartitt graf?

### Definisjon

En **bipartitt graf** (todelt graf) er en graf der nodene kan deles inn i **to disjunkte mengder** $U$ og $V$ slik at:

- **Alle kanter** går mellom $U$ og $V$
- **Ingen kanter** går innenfor $U$ eller innenfor $V$

Med andre ord: Hver kant forbinder én node fra $U$ med én node fra $V$.

### Notasjon

En bipartitt graf skrives ofte som $G = (U, V, E)$ der:
- $U$ og $V$ er nodemengdene
- $E \subseteq U \times V$ (alle kanter går på tvers)

### Eksempel 1: Enkel bipartitt graf

```mermaid
graph LR
    subgraph U
        A
        B
    end
    
    subgraph V
        C
        D
        E
    end
    
    A --- C
    A --- D
    B --- D
    B --- E