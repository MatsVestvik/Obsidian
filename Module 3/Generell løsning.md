## Generell løsning for lineære Diofantiske likninger

For likningen
$$ax + by = c$$
der $d = \gcd(a, b)$ og $d \mid c$, har den generelle heltallsløsningen formen:

$$x = x_0 + \frac{b}{d} \cdot t$$
$$y = y_0 - \frac{a}{d} \cdot t$$

der $t \in \mathbb{Z}$ og $(x_0, y_0)$ er én spesiell løsning.

### Anvendelse på vår likning

Vi har
$$157x + 124y = 4000$$
med $\gcd(157, 124) = 1$ og én spesiell løsning $(x_0, y_0) = (-60000, 76000)$.

Da blir den generelle løsningen:
$$x = -60000 + \frac{124}{1} \cdot t = -60000 + 124t$$
$$y = 76000 - \frac{157}{1} \cdot t = 76000 - 157t$$

### Verifikasjon

Setter vi inn i likningen:
$$
\begin{aligned}
157(-60000 + 124t) + 124(76000 - 157t) &= 157 \cdot (-60000) + 157 \cdot 124t + 124 \cdot 76000 - 124 \cdot 157t \\
&= (-157 \cdot 60000 + 124 \cdot 76000) + (157 \cdot 124 - 124 \cdot 157)t \\
&= 4000 + 0 \cdot t = 4000
\end{aligned}
$$

### Hvorfor akkurat disse koeffisientene?

Øker vi $x$ med $124$, må vi minke $y$ med $157$ for å holde summen $157x + 124y$ uendret. Dette skyldes at
$$157 \cdot 124 = 124 \cdot 157$$
slik at endringene kansellerer hverandre.