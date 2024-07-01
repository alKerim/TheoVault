Related: [[Berechenbarkeit]]
_____

Eine Funktion $f: \mathbb{N}^k \rightarrow \mathbb{N}$ ist **intuitiv berechenbar**, wenn es einen Algorithmus gibt, der bei Eingabe $\left(n_1, \ldots, n_k\right) \in \mathbb{N}^k$
- nach endlich vielen Schritten mit Ergebnis $f\left(n_1, \ldots, n_k\right)$ hält, falls $f\left(n_1, \ldots, n_k\right)$ definiert ist,
- und nicht terminiert, falls $f\left(n_1, \ldots, n_k\right)$ nicht definiert ist.

Was bedeutet „Algorithmus“? Assembler? C? Java? OCaml? Macht es einen Unterschied?

______

Die Menge der [[erreichbar (theo)|erreichbaren Symbole]] einer [[Kontextfreie Grammatiken|CFG]] ist **berechenbar**.
	Beweis:
	Wir berechnen die erreichbaren Symbole induktiv:
	- $S$ ist erreichbar.
	- Ist $A$ erreichbar und $(A \rightarrow \alpha X \beta) \in P$, so ist auch $X$ erreichbar.







# Beispiele

### Beispiel 1
Ist die Funktion
$$\begin{equation*}
f_1(n):=\left\{\begin{array}{ll}
1 & \text { falls } n \text { als Ziffernfolge Anfangsstück der } \\
& \text { Dezimalbruchentwicklung von } \pi \text { ist } \\
0 & \text { sonst }
\end{array}\right.
\end{equation*}$$
berechenbar? (Bsp: $f_1(31415)=1$ aber $\left.f_1(315)=0\right)$
Ja, denn es Algorithmen gibt, die $\pi$ iterativ auf beliebig viele Dezimalstellen genau berechnet werden.

### Beispiel 2
Ist die Funktion
$$\begin{equation*}
f_2(n):=\left\{\begin{array}{ll}
1 & \text { falls } n \text { als Ziffernfolge irgendwo in der } \\
& \text { Dezimalbruchentwicklung von } \pi \text { vorkommt } \\
0 & \text { sonst }
\end{array}\right.
\end{equation*}$$
berechenbar? $\left(\right.$ Bsp: $\left.f_2(415)=1\right)$
**Unbekannt**!
Durch schrittweise Approximation und Suche in der Dezimalbruchentwicklung von $\pi$ kann man feststellen, dass $n$ vorkommt
Aber wie stellt man fest, dass $n$ nicht vorkommt? Nichttermination statt 0 !

Vielleicht gibt es aber einen (noch zu findenden) mathematischen Satz, der genaue Aussagen über die in $\pi$ vorkommenden Ziffernfolgen macht.

