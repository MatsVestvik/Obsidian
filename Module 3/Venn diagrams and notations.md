
## Liste over tegn:
- A ∩ B (snitt - det som er i både A og B)
- A ∪ B (union - alt som er i A eller B)
- A \ B (A minus B - det som er i A, men ikke i B)
- Aᶜ (komplement - alt som ikke er i A)
- A△B=(A∖B)∪(B∖A)
---------------------------------
### Eksempel på venndiagram

```tikz
\begin{document}
\begin{tikzpicture}

\def\r{2}

\coordinate (A) at (0,1.5);
\coordinate (B) at (-1.7,-0.5);
\coordinate (C) at (1.7,-0.5);

% Fill C
\fill[cyan!60] (C) circle (\r);

% Fill A ∩ B
\begin{scope}
  \clip (A) circle (\r);
  \fill[cyan!60] (B) circle (\r);
\end{scope}

% Remove triple intersection
\begin{scope}
  \clip (A) circle (\r);
  \clip (B) circle (\r);
  \fill[white] (C) circle (\r);
\end{scope}

% Remove C ∩ A
\begin{scope}
	\clip (A) circle (\r);
	\fill[white] (C) circle (\r);
\end{scope}

% Outlines
\draw (A) circle (\r);
\draw (B) circle (\r);
\draw (C) circle (\r);

\node at (0,3.2) {$A$};
\node at (-3,-0.5) {$B$};
\node at (3,-0.5) {$C$};

\end{tikzpicture}
\end{document}
```


Hvis jeg vill beskrevet de skraverte områdene (AB, AC, C). Kunne jeg skrevet det slik:
$$
(A ∩ B ∩ C^c) ∪ (A^c ∩ B ∩ C) ∪ (A^c ∩ B^c ∩ C)
$$