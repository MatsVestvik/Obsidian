# Taylor-polynom av grad 2 fra gradient og Hessematrise

## Oppgitt funksjon

$$
f(x, y) = 16y^2 + 24xy + 9x^2.
$$

Punkt: $(-2, -1)$.

---

## 1. Gradient og Hessematrise (allerede beregnet)

### Gradient

$$
\nabla f = \begin{bmatrix} 24y + 18x & 32y + 24x \end{bmatrix}
$$

### Hessematrise

$$
H_f = \begin{bmatrix}
18 & 24 \\
24 & 32
\end{bmatrix}
$$

---

## 2. Evaluér i punktet $(a,b) = (-2,-1)$

### Funksjonsverdien

$$
f(-2,-1) = 16(1) + 24(2) + 9(4) = 16 + 48 + 36 = 100.
$$

### Gradienten i punktet

$$
\nabla f(-2,-1) = \begin{bmatrix} 24(-1) + 18(-2) & 32(-1) + 24(-2) \end{bmatrix}
$$

Første komponent: $24(-1) = -24$, $18(-2) = -36$, sum $= -60$.

Andre komponent: $32(-1) = -32$, $24(-2) = -48$, sum $= -80$.

$$
\nabla f(-2,-1) = \begin{bmatrix} -60 & -80 \end{bmatrix}
$$

### Hessematrisen i punktet

Hessematrisen har konstante elementer, så den er den samme i alle punkt:

$$
H_f(-2,-1) = \begin{bmatrix}
18 & 24 \\
24 & 32
\end{bmatrix}
$$

---

## 3. Formel for Taylor-polynom av grad 2 i to variable

For et punkt $(a,b)$:

$$
P_2(x,y) = f(a,b) + \nabla f(a,b) \cdot \begin{bmatrix} x-a \\ y-b \end{bmatrix} + \frac{1}{2} \begin{bmatrix} x-a & y-b \end{bmatrix} H_f(a,b) \begin{bmatrix} x-a \\ y-b \end{bmatrix}
$$

Her er $(a,b) = (-2,-1)$, så $x-a = x+2$ og $y-b = y+1$.

---

## 4. Sett inn verdiene

$$
P_2(x,y) = 100 + \begin{bmatrix} -60 & -80 \end{bmatrix} \begin{bmatrix} x+2 \\ y+1 \end{bmatrix} + \frac{1}{2} \begin{bmatrix} x+2 & y+1 \end{bmatrix} \begin{bmatrix} 18 & 24 \\ 24 & 32 \end{bmatrix} \begin{bmatrix} x+2 \\ y+1 \end{bmatrix}
$$

### Første ordens ledd

$$
-60(x+2) - 80(y+1)
$$

### Andre ordens ledd

Regn ut matriseproduktet først:

$$
\begin{bmatrix} 18 & 24 \\ 24 & 32 \end{bmatrix} \begin{bmatrix} x+2 \\ y+1 \end{bmatrix} = \begin{bmatrix} 18(x+2) + 24(y+1) \\ 24(x+2) + 32(y+1) \end{bmatrix}
$$

Deretter multipliser med $\begin{bmatrix} x+2 & y+1 \end{bmatrix}$:

$$
(x+2)[18(x+2) + 24(y+1)] + (y+1)[24(x+2) + 32(y+1)]
$$

Regn ut ledd for ledd:

- $18(x+2)^2$
- $24(x+2)(y+1)$
- $24(y+1)(x+2)$ (samme som forrige)
- $32(y+1)^2$

Sum: $18(x+2)^2 + 48(x+2)(y+1) + 32(y+1)^2$

Nå multipliser med $\frac{1}{2}$:

$$
9(x+2)^2 + 24(x+2)(y+1) + 16(y+1)^2
$$

---

## 5. Sett sammen hele Taylor-polynomet

$$
P_2(x,y) = 100 - 60(x+2) - 80(y+1) + 9(x+2)^2 + 24(x+2)(y+1) + 16(y+1)^2
$$

---

## 6. Forenkling (valgfritt)

Vi kan bekrefte at dette er lik $f(x,y)$ ved å sette $x = u-2$, $y = v-1$:

$$
\begin{aligned}
P_2 &= 100 - 60u - 80v + 9u^2 + 24uv + 16v^2 \\
&= 9u^2 + 24uv + 16v^2 - 60u - 80v + 100
\end{aligned}
$$

Dette er akkurat $f(u-2, v-1)$ når vi regner ut (vist i forrige notat).

---

## Svar

Taylor-polynomet av grad 2 for $f(x,y)$ om punktet $(-2,-1)$ er:

$$
\boxed{P_2(x,y) = 100 - 60(x+2) - 80(y+1) + 9(x+2)^2 + 24(x+2)(y+1) + 16(y+1)^2}
$$