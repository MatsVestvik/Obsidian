

Hesse matrisen er en matrise som inneholder de partiellderiverte til en funksjon:

$$
H = \begin{pmatrix}
\frac{\partial^2 f}{\partial x^2} & \frac{\partial^2 f}{\partial x \partial y} \\[6pt]
\frac{\partial^2 f}{\partial y \partial x} & \frac{\partial^2 f}{\partial y^2}
\end{pmatrix}
$$

har funksjonen tre variabler vil hesse matrisen være 3x3 også videre

Den kan brukes til å finne ut om et punkt er et topp, bunn eller sadelpunkt.
Hvis du har funnet et punkt hvor [[Gradient]] er lik null, kan du deretter evaluere punktet i en hesse matrise.

Regn ut determinanten D av hesse matrisen i punktet du evaluerer (ad-bc).

>[!Important]
>Lokalt minimum:
>$$
>D > 0 \quad \text{og} \quad f_{xx} > 0
>$$
>
>Lokalt maksimum:
>$$
>D > 0 \quad \text{og} \quad f_{xx} < 0
>$$
>
>Sadelpunkt:
>$$
>D > 0
>$$
>
>inkoklusiv:
>$$
>D = 0
>$$