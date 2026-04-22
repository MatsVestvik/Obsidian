# Lagranges restleddsformel (Taylor)

## Formelen
Hvis vi approksimerer en funksjon $f(x)$ med et Taylor-polynom $P_n(x)$ av grad $n$ om punktet $x = a$, kan vi skrive:
$$f(x) = P_n(x) + R_n(x)$$
der **restleddet** $R_n(x)$ er gitt ved **Lagranges formel**:
$$R_n(x) = \frac{f^{(n+1)}(c)}{(n+1)!}(x-a)^{n+1}$$

## Hva betyr de ulike delene?

| Symbol | Betydning | Forklaring |
| :--- | :--- | :--- |
| $R_n(x)$ | **Restleddet** | Den eksakte feilen vi gjør ved å bruke polynomet $P_n(x)$ i stedet for $f(x)$. |
| $n$ | **Graden til polynomet** | Antall ledd i Taylor-polynomet *minus 1*. (Eks: $P_1(x)$ har $n=1$). |
| $f^{(n+1)}$ | **Den $(n+1)$-te deriverte** | Hvis $n=1$, er dette den 2. deriverte ($f''$). Hvis $n=2$, er det den 3. deriverte ($f'''$). |
| $c$ | **Et ukjent punkt** | $c$ er et tall som ligger **strengt mellom** $a$ og $x$. Vi vet ikke nøyaktig hva $c$ er, men vi vet at det finnes. |
| $(n+1)!$ | **Fakultet av $(n+1)$** | $(n+1)! = 1 \cdot 2 \cdot 3 \cdots (n+1)$. Dette tallet vokser veldig raskt og gjør restleddet mindre for høye $n$. |
| $(x-a)^{n+1}$ | **Avstanden fra sentrum** | Avstanden fra punktet vi utvikler om ($a$) til punktet vi evaluerer i ($x$), opphøyd i $n+1$. Hvis $x$ er nær $a$, blir denne potensen veldig liten. |

## Hvordan bruker vi den i praksis?
Siden vi ikke vet verdien av $c$, kan vi ikke beregne $R_n(x)$ eksakt. Vi bruker derfor formelen til å finne en **øvre grense for feilen**:

1. Finn den maksimale verdien av $|f^{(n+1)}(c)|$ for alle $c$ i intervallet mellom $a$ og $x$. La oss kalle dette maksimum $M$.
2. Da er feilen **garantert mindre enn**:
$$|R_n(x)| \le \frac{M}{(n+1)!} |x-a|^{n+1}$$

## Eksempel med $\sin(x)$ og $n=1$
- $a = 0$, $x = 1/7$, $n=1$.
- $f''(x) = -\sin(x)$. Maksimum av $|-\sin(c)|$ i intervallet $[0, 1/7]$ er $\sin(1/7)$.
- $(n+1)! = 2! = 2$.
- $(x-a)^{n+1} = (1/7)^2 = 1/49$.

Gir grensen: $|R_1(x)| \le \frac{\sin(1/7)}{2} \cdot \frac{1}{49} \approx 0.00145$.

## Alternativ form: Cauchys restledd
Det finnes en annen variant som av og til gir en strammere grense, men Lagranges er den vanligste:
$$R_n(x) = \frac{f^{(n+1)}(c)}{n!}(x-c)^n(x-a)$$
(Brukes sjeldnere i grunnleggende kalkulus.)

## Viktig skille
- **Taylor-polynom:** Det vi regner ut med $a$ og $x$.
- **Restledd:** Det vi *ikke* regner ut, men som estimerer hvor stor feil vi gjør.