###  Algoritme
Vi bruker dette for å finne GCD (Største felles divisor).
For tallet a,b hvor vi ønsker å finne gcd(a,b), starter vi med å skrive a det større tallet som et multiplum av b med rest. Vi tar deretter å skriver b som et multiplum av resten vår pluss enda en rest. Vi forstsetter disse stegene til resten er 0. Den siste resten vil da være den største felles divisor mellom verdiene a,b.
>[!Formel]
>$$
>a = q_1b + r_1
>$$
>
>$$
>b = q_2r_1 + r_2
>$$
>
>$$
>r_1 = q_3r_2 0 r_3
>$$
>$$
>...
>$$
>$$
>r_{n-1} = q_{n+1}r_n + 0
>$$
>$$
>gcd(a,b) = r_n
>$$

### Utvidet Algoritme

>[!Formel]
> $$
> ax+bx = gcd(a,b)
> $$

Hvis vi har en oppgave:
25x+15y = 5
Hvor vi ønsker å finne x,y kan vi bruke Euklisi Utvidet algoritme.

Vi regner ut euklidis algoritme og skriver om leddene
 25 = 1 x 15 + 10 -> 10 = 25 - 1 x 15
 15 = 1 x 10 + 5   -> 5 = 15 - 1 x 10
 10 = 2 x 5 + 0

nå har vi to uttrykk vi kan skrive om. 5 = 15 -1 x (25-1 x 15) -> 5 = 2 x 15 + -1 x 25
Da vet vi at svaret er x = -1 og y = 2
