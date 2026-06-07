## Intuitiv forståelse
Taylor-polynomer er en metode for å **approksimere en komplisert funksjon $f(x)$ med et polynom** i nærheten av et punkt $x = a$.

Ideen er: Hvis vi vet alt om funksjonen i ett enkelt punkt (funksjonsverdi, stigningstall, krumning osv.), kan vi gjette hvordan funksjonen ser ut like i nærheten.

## Definisjon
Taylor-polynomet av grad $n$ for funksjonen $f$ om punktet $x = a$ er gitt ved:

$$P_n(x) = f(a) + f'(a)(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \frac{f'''(a)}{3!}(x-a)^3 + \dots + \frac{f^{(n)}(a)}{n!}(x-a)^n$$

På summeform:
$$P_n(x) = \sum_{k=0}^{n} \frac{f^{(k)}(a)}{k!}(x-a)^k$$
hvor $f^{(k)}(a)$ er den $k$-te deriverte evaluert i $a$, og $k!$ er fakultet av $k$.

## Spesialtilfellet Maclaurin-polynom
Når $a = 0$ kalles det et **Maclaurin-polynom**:
$$P_n(x) = \sum_{k=0}^{n} \frac{f^{(k)}(0)}{k!}x^k$$

## Viktige Maclaurin-rekker (utviklinger)
Disse bør pugges:

| Funksjon $f(x)$ | Taylor-rekke (Maclaurin) |
| :--- | :--- |
| $e^x$ | $1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \dots = \sum_{k=0}^{\infty} \frac{x^k}{k!}$ |
| $\sin x$ | $x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dots = \sum_{k=0}^{\infty} (-1)^k \frac{x^{2k+1}}{(2k+1)!}$ |
| $\cos x$ | $1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots = \sum_{k=0}^{\infty} (-1)^k \frac{x^{2k}}{(2k)!}$ |
| $\ln(1+x)$ | $x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \dots = \sum_{k=1}^{\infty} (-1)^{k+1} \frac{x^k}{k}$ |
| $(1+x)^\alpha$ (Binomisk) | $1 + \alpha x + \frac{\alpha(\alpha-1)}{2!}x^2 + \dots$ |

## Restledd og feilestimering (Taylors formel med restledd)
Taylor-polynomet er bare en tilnærming. Forskjellen mellom den virkelige funksjonen og polynomet kalles **restleddet** $R_n(x)$:
$$f(x) = P_n(x) + R_n(x)$$

**Lagranges restleddsformel:**
Det finnes et tall $c$ mellom $a$ og $x$ slik at:
$$R_n(x) = \frac{f^{(n+1)}(c)}{(n+1)!}(x-a)^{n+1}$$
Dette brukes til å finne en øvre grense for feilen i approksimasjonen.

## Praktisk tolkning av leddene
1. **0. grad ($n=0$):** Konstant. $P_0(x) = f(a)$. (Vannrett linje gjennom punktet).
2. **1. grad ($n=1$):** Tangentlinje. $P_1(x) = f(a) + f'(a)(x-a)$. (Lineær approksimasjon).
3. **2. grad ($n=2$):** Legger til krumning (andrederivert). $P_2(x) = P_1(x) + \frac{f''(a)}{2}(x-a)^2$.
4. **Høyere grad:** Jo flere ledd vi tar med, jo bedre "klistrer" polynomet seg til funksjonens faktiske form lenger bort fra $a$.

## Eksempel: Approksimer $e^{0.1}$
Vi vet $f(x) = e^x$, $a=0$.
$P_3(x) = 1 + x + \frac{x^2}{2} + \frac{x^3}{6}$
Med $x = 0.1$:
$P_3(0.1) = 1 + 0.1 + \frac{0.01}{2} + \frac{0.001}{6} = 1 + 0.1 + 0.005 + 0.000166... \approx 1.10517$
(Sann verdi: $e^{0.1} \approx 1.10517$. Allerede svært nøyaktig med kun 3. grad!)

## Bruksområder
- **Fysikk:** Små vinkel-approksimasjon ($\sin x \approx x$ for små $x$).
- **Numerikk:** Datamaskiner bruker Taylor-rekker for å beregne verdier av $\sin$, $\cos$, $\exp$, $\log$ internt.
- **Grenseverdier:** Erstatter kompliserte funksjoner med polynomer for å evaluere $\lim_{x \to 0}$ (f.eks. $\frac{\sin x - x}{x^3} = -\frac{1}{6}$).
- **Differensialligninger:** Løsninger uttrykkes ofte som uendelige rekker.