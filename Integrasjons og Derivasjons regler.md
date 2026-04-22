# Derivasjon og integrasjon

En oversikt over de viktigste reglene for derivasjon og integrasjon, med koblinger mellom dem.

## 📌 Derivasjonsregler

| Funksjon $f(x)$ | Derivert $f'(x)$ |
|----------------|------------------|
| $C$ (konstant) | $0$ |
| $x^n$ | $n x^{n-1}$ |
| $e^x$ | $e^x$ |
| $a^x$ | $a^x \ln a$ |
| $\ln x$ | $\frac{1}{x}$ |
| $\sin x$ | $\cos x$ |
| $\cos x$ | $-\sin x$ |
| $\tan x$ | $\sec^2 x$ |

### Regler

- **Konstantfaktor**: $(c \cdot f)' = c \cdot f'$
- **Sum**: $(f + g)' = f' + g'$
- **Produkt**: $(f \cdot g)' = f'g + fg'$
- **Kvotient**: $\left(\frac{f}{g}\right)' = \frac{f'g - fg'}{g^2}$
- **Kjerneregel**: $(f(g(x)))' = f'(g(x)) \cdot g'(x)$

---

## 🔁 Integrasjonsregler (ubestemt integral)

| Integrand $f(x)$ | $\int f(x) \, dx$ |
|------------------|------------------|
| $C$ (konstant) | $Cx + k$ |
| $x^n$ ($n \neq -1$) | $\frac{x^{n+1}}{n+1} + k$ |
| $\frac{1}{x}$ | $\ln |x| + k$ |
| $e^x$ | $e^x + k$ |
| $a^x$ | $\frac{a^x}{\ln a} + k$ |
| $\sin x$ | $-\cos x + k$ |
| $\cos x$ | $\sin x + k$ |
| $\sec^2 x$ | $\tan x + k$ |

### Regler

- **Konstantfaktor**: $\int c \cdot f(x) \, dx = c \int f(x) \, dx$
- **Sumregel**: $\int (f(x) + g(x)) \, dx = \int f(x) \, dx + \int g(x) \, dx$
- **Delvis integrasjon (produkt)**: $\int u \, dv = uv - \int v \, du$
- **Substitusjon (kjerneregel baklengs)**: $\int f(g(x)) \cdot g'(x) \, dx = \int f(u) \, du$ der $u = g(x)$

---

## 🔗 Sammenheng

> **Derivasjon og integrasjon er inverse operasjoner**  
> $\frac{d}{dx} \left( \int f(x) \, dx \right) = f(x)$  
> $\int f'(x) \, dx = f(x) + C$

## 📝 Eksempler

- $\frac{d}{dx} \left( \frac{x^{n+1}}{n+1} \right) = x^n$ → $\int x^n \, dx = \frac{x^{n+1}}{n+1} + C$
- $\frac{d}{dx} (\sin x) = \cos x$ → $\int \cos x \, dx = \sin x + C$