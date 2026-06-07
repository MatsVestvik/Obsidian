## Fremgangsmåte

1. Regn ut de partiellderiverte $f_x$ og $f_y$
2. Evaluér dem i punktet $(x_0, y_0)$
3. Sett inn i formelen:

$$
z - z_0 = f_x(x_0,y_0)(x - x_0) + f_y(x_0,y_0)(y - y_0)
$$

## Eksempel

La $f(x,y) = \sqrt{28 - x^2 - 2y^2}$ og punktet $(-1,-3,3)$.

### Steg 1: Sjekk at punktet ligger på flaten

$$
f(-1,-3) = \sqrt{28 - (-1)^2 - 2 \cdot (-3)^2} = \sqrt{28 - 1 - 18} = \sqrt{9} = 3 \quad \checkmark
$$

### Steg 2: Partiellderiverte

$$
f_x = \frac{-x}{\sqrt{28 - x^2 - 2y^2}}, \qquad f_y = \frac{-2y}{\sqrt{28 - x^2 - 2y^2}}
$$

### Steg 3: Evaluér i $(-1,-3)$

Nevneren er $\sqrt{9} = 3$, så:

$$
f_x(-1,-3) = \frac{-(-1)}{3} = \frac{1}{3}
$$

$$
f_y(-1,-3) = \frac{-2(-3)}{3} = \frac{6}{3} = 2
$$

### Steg 4: Sett inn i formelen

$$
z - 3 = \frac{1}{3}(x + 1) + 2(y + 3)
$$

### Steg 5: Forenkle til formen $z = ax + by + c$

$$
z - 3 = \frac{1}{3}x + \frac{1}{3} + 2y + 6
$$

$$
z - 3 = \frac{1}{3}x + 2y + \frac{1}{3} + 6
$$

$$
z - 3 = \frac{1}{3}x + 2y + \frac{1}{3} + \frac{18}{3}
$$

$$
z - 3 = \frac{1}{3}x + 2y + \frac{19}{3}
$$

$$
z = \frac{1}{3}x + 2y + \frac{19}{3} + 3
$$

$$
z = \frac{1}{3}x + 2y + \frac{19}{3} + \frac{9}{3}
$$

$$
z = \frac{1}{3}x + 2y + \frac{28}{3}
$$

**Svar:** $a = \frac{1}{3},\; b = 2,\; c = \frac{28}{3}$

---

## Bruk av tangentplanet til estimering

Estimer $f\left(-\frac{4}{5}, -\frac{33}{10}\right)$ ved å sette inn i tangentplanet:

$$
z\left(-\frac{4}{5}, -\frac{33}{10}\right) = \frac{1}{3}\left(-\frac{4}{5}\right) + 2\left(-\frac{33}{10}\right) + \frac{28}{3}
$$

Regn ut hver del:

$$
\frac{1}{3} \cdot \left(-\frac{4}{5}\right) = -\frac{4}{15}
$$

$$
2 \cdot \left(-\frac{33}{10}\right) = -\frac{66}{10} = -\frac{33}{5}
$$

Skriv alt med fellesnevner $15$:

$$
-\frac{4}{15} - \frac{33}{5} + \frac{28}{3} = -\frac{4}{15} - \frac{99}{15} + \frac{140}{15}
$$

$$
= \frac{-4 - 99 + 140}{15} = \frac{37}{15}
$$

**Svar:** $\displaystyle f\left(-\frac{4}{5}, -\frac{33}{10}\right) \approx \frac{37}{15}$

---

## Formler å huske

| Situasjon | Formel |
|-----------|--------|
| Eksplisitt $z = f(x,y)$ | $z - z_0 = f_x(x_0,y_0)(x-x_0) + f_y(x_0,y_0)(y-y_0)$ |
| Implisitt $F(x,y,z)=0$ | $F_x(P)(x-x_0) + F_y(P)(y-y_0) + F_z(P)(z-z_0) = 0$ |