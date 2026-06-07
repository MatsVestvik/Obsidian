
## Oppgitt funksjon og Taylor-polynom

$$
f(x, y) = 16y^2 + 24xy + 9x^2
$$

Taylor-polynomet av grad 2 om punktet $(-2,-1)$ er:

$$
P_2(x, y) = 100 - 60(x+2) - 80(y+1) + 9(x+2)^2 + 24(x+2)(y+1) + 16(y+1)^2
$$

---

## 1. Regn ut $R(x, y) = f(x, y) - P_2(x, y)$

Vi må først utvikle $P_2(x, y)$ til standard form $Ax^2 + Bxy + Cy^2 + Dx + Ey + F$.

### Utvikling av $P_2(x, y)$

La $u = x+2$, $v = y+1$. Da er:

$$
P_2 = 100 - 60u - 80v + 9u^2 + 24uv + 16v^2.
$$

#### Regn ut $u^2$, $uv$, $v^2$:

- $u^2 = (x+2)^2 = x^2 + 4x + 4$
- $v^2 = (y+1)^2 = y^2 + 2y + 1$
- $uv = (x+2)(y+1) = xy + x + 2y + 2$

#### Sett inn:

$$
\begin{aligned}
9u^2 &= 9x^2 + 36x + 36 \\
24uv &= 24xy + 24x + 48y + 48 \\
16v^2 &= 16y^2 + 32y + 16 \\
-60u &= -60x - 120 \\
-80v &= -80y - 80 \\
\text{konstant} &= 100
\end{aligned}
$$

#### Summer ledd for ledd:

**$x^2$:** $9x^2$  
**$xy$:** $24xy$  
**$y^2$:** $16y^2$  
**$x$:** $36x + 24x - 60x = 0$  
**$y$:** $48y + 32y - 80y = 0$  
**konstant:** $36 + 48 + 16 - 120 - 80 + 100 = 0$

Sjekk konstantleddet nøye:

$36 + 48 = 84$  
$84 + 16 = 100$  
$100 - 120 = -20$  
$-20 - 80 = -100$  
$-100 + 100 = 0$ ✅

Altså:

$$
P_2(x, y) = 9x^2 + 24xy + 16y^2
$$

---

## 2. Sammenlign med $f(x, y)$

$$
f(x, y) = 16y^2 + 24xy + 9x^2 = 9x^2 + 24xy + 16y^2
$$

Vi ser at:

$$
f(x, y) = P_2(x, y) \quad \text{for alle } x, y.
$$

---

## 3. Feilleddet

$$
R(x, y) = f(x, y) - P_2(x, y) = 0
$$

---

## Svar

$$
\boxed{R(x, y) = 0}
$$

---

## Til ettertanke

> Legg merke til at funksjonen $f(x, y)$ er et andregradspolynom i $x$ og $y$.  
> Tror du at uttrykket for feilleddet $R(x, y)$ vil gjelde for alle andregradspolynomer i $x$ og $y$?

**Svar:**  
Ja. For **ethvert** andregradspolynom i $x$ og $y$ vil Taylor-polynomet av grad 2 om **ethvert** punkt være identisk med funksjonen selv. Dette fordi tredje- og høyere ordens deriverte er null. Derfor blir feilleddet alltid $0$ for alle andregradspolynomer, uansett hvilket punkt du utvikler rundt.

Mer presist: Hvis $f$ er et polynom av grad $\le 2$, så er $P_2$ (Taylor av grad 2) eksakt lik $f$, og $R(x,y) \equiv 0$.