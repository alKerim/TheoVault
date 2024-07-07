#theo/berechenbarkeit 
Karte (uendlich viele):
- Immer oben ein Wort.
- Unten auch

Wir müssen die so hintereinander legen, dass oben und unten das gleiche Wort entsteht

# Formale Definition
**Gegeben**: Eine endliche Folge $\left(x_1, y_1\right), \ldots,\left(x_k, y_k\right)$, wobei $x_i, y_i \in \Sigma^{+}$.

**Problem**: Gibt es eine Folge von Indizes $i_1, \ldots, i_n \in\{1, \ldots, k\}$, $n>0$, mit $x_{i_1} \ldots x_{i_n}=y_{i_1} \ldots y_{i_n}$ ?

Dann nennen wir $i_1, \ldots, i_n$ eine Lösung der Instanz $\left(x_1, y_1\right), \ldots,\left(x_k, y_k\right)$ des PCP Problems.


# Beispiele
#### Beispiel 1
a) $\frac{1}{111}$, b) $\frac{10111}{10}$, c) $\frac{10}{0}$
Kombination: b,a,a,c -> $\frac{10111,1,1,10}{10,111,111,0}$




# Entscheidbarkeit
- PCP ist [[semi-entscheidbar (s-e)]]
	Beweis:
	Zähle die möglichen Lösungen der Länge nach auf, und probiere jeweils, ob es eine wirkliche Lösung ist.
	Wir zeigen nun:$$\begin{equation*}
	H \leq M P C P \leq P C P\end{equation*}$$wobei [[MPCP]]
- Das $P C P$ ist [[unentscheidbar]].
- Das $P C P$ ist auch für $\Sigma=\{0,1\}$ unentscheidbar.

#### Manche PCP entscheidbar
#theo/berechenbarkeit/basics
$k$ ist die Anzahl Karten die zur Auswahl stehen.
- Das PCP ist [[entscheidbar]] falls $|\Sigma|=1$
- Das PCP ist entscheidbar falls $k \leq 2$.
- Das PCP ist unentscheidbar falls $k \geq 5$.
- Für $k=3,4$ ist noch offen, ob das PCP unentscheidbar ist.










______
Related: Postsche Problem entdeckt von [[Emil Post]]
