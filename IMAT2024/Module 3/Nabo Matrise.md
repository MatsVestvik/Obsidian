## Hva er en nabomatrise?

En **nabomatrise** $A$ er en kvadratisk matrise som beskriver forbindelsene (kantene) i en graf. For en graf med $n$ noder er $A$ en $n \times n$-matrise der:

$$A_{ij} = \begin{cases} 
1 & \text{hvis det finnes en kant mellom node } i \text{ og node } j \\
0 & \text{ellers}
\end{cases}$$

## Enkel graf (uten løkker, multiple kanter)

For en **enkel** urettet graf gjelder:
- $A_{ii} = 0$ for alle $i$ (ingen løkker)
- $A_{ij} = A_{ji}$ (symmetrisk fordi kant er urettet)

### Eksempel 1: Graf med 3 noder (trekant)

Grafen: Nodene 1, 2, 3 der alle par er koblet sammen ($K_3$)

Kanter: (1,2), (1,3), (2,3)

Nabomatrisen $A$ (3×3):

$$A = \begin{pmatrix}
0 & 1 & 1 \\
1 & 0 & 1 \\
1 & 1 & 0
\end{pmatrix}$$

**Lesing av matrisen:**
- Rad 1, kolonne 2: $A_{12}=1$ → kant mellom node 1 og 2
- Rad 2, kolonne 3: $A_{23}=1$ → kant mellom node 2 og 3
- Rad 1, kolonne 1: $A_{11}=0$ → ingen løkke på node 1

### Eksempel 2: Graf med 4 noder (sti $P_4$)

Grafen: 1-2-3-4 (en sti)

Kanter: (1,2), (2,3), (3,4)

$$A = \begin{pmatrix}
0 & 1 & 0 & 0 \\
1 & 0 & 1 & 0 \\
0 & 1 & 0 & 1 \\
0 & 0 & 1 & 0
\end{pmatrix}$$

### Eksempel 3: Graf med 4 noder (syklus $C_4$)

Grafen: 1-2-3-4-1 (en firkant)

Kanter: (1,2), (2,3), (3,4), (4,1)

$$A = \begin{pmatrix}
0 & 1 & 0 & 1 \\
1 & 0 & 1 & 0 \\
0 & 1 & 0 & 1 \\
1 & 0 & 1 & 0
\end{pmatrix}$$

## Hva forteller nabomatrisen oss?

### 1. Graden til en node

For en urettet graf: **Graden til node $i$ = summen av rad $i$** (eller kolonne $i$)

$$\deg(i) = \sum_{j=1}^n A_{ij}$$

**Eksempel for $C_4$:**
- Rad 1: [0, 1, 0, 1] → sum = 2 → node 1 har grad 2 ✅

### 2. Naboene til en node

Naboene til node $i$ er alle $j$ slik at $A_{ij} = 1$.

**Eksempel for $C_4$:**
- Node 1: $A_{12}=1$ og $A_{14}=1$ → naboer: 2 og 4

### 3. Antall kanter i grafen

For urettet graf:

$$|E| = \frac{1}{2} \sum_{i=1}^n \sum_{j=1}^n A_{ij}$$

(Deler på 2 fordi hver kant telles to ganger: én gang fra $i$ til $j$ og én gang fra $j$ til $i$)

## Ulike typer grafer og deres nabomatriser

### Urettet graf (standard)

| | 1 | 2 | 3 |
|---|---|---|---|
| 1 | 0 | 1 | 0 |
| 2 | 1 | 0 | 1 |
| 3 | 0 | 1 | 0 |

**Egenskaper:**
- $A$ er symmetrisk: $A_{ij} = A_{ji}$
- Diagonalen er 0 (hvis ingen løkker)

### Rettet graf (digraf)

For rettet graf: $A_{ij} = 1$ hvis det finnes en kant **fra** $i$ **til** $j$