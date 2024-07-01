# reduzierbar
![[reduzierbar]]

# Die Reduktion
Wir schreiben dann $A \leq B$. 
"$A$ lässt sich auf $B$ reduzieren"

Intuition:
- Aus einem Algorithmus für $B$ kann man einen Algorithmus für $A$ gewinnen.
- Ist $B$ [[entscheidbar]], dann erst recht $A$.
- Ist $A$ [[unentscheidbar]], dann auch $B$.
- $B$ ist mindestens so schwer zu lösen wie $A$.


# Entscheidbarkeit
Falls $A \leq B$ und $B$ ist entscheidbar, so ist auch $A$ entscheidbar.

#### Beweis
Beweis:
Es gelte $A \leq B$ mittels $f$ und $\chi_B$ sei [[berechenbar]]. Dann ist $\chi_B \circ f$ berechenbar und $\chi_A=\chi_B \circ f$ :
$$\begin{equation*}
\chi_A(x)=\left\{\begin{array}{ll}
1, & x \in A \\
0, & x \notin A
\end{array}=\left\{\begin{array}{ll}
1, & f(x) \in B \\
0, & f(x) \notin B
\end{array}=\chi_B(f(x))\right.\right.
\end{equation*}$$

# Untentscheidbarkeit
Falls $A \leq B$ und $A$ ist [[unentscheidbar]], dann ist auch $B$ unentscheidbar.


# Beispiele
#### Beispiel 1 (aus VL)
Wir haben A auf B reduziert
![[Screenshot 2024-06-20 at 15.12.38.png|500]]

#### Beispiel 2
Da $K \leq H$ (mit Reduktion $f(w):=w \# w$ ) und $K$ [[unentscheidbar]] ist, ist auch $H$ unentscheidbar.

###### von tweedback:
Beim Halteproblem auf leerem Band: Ich verstehe nicht, warum man das Programm ohne Eingabe auf ein Programm mit Eingabe reduzieren kann. Ändert das nicht die Semantik des Programms?

Antwort:
	Ich verstehe die Frage nicht ganz. In beiden Fällen haben wir doch eine Eingabe? Im ersten Fall ist es die Kodierung der TM selbst und im zweiten Fall ist es das leere Wort.
