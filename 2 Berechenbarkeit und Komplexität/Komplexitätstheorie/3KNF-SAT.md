Gegeben: Eine Formel in [[3KNF]]
Problem: Ist die Formel [[erfüllbar]]?

Offensichtlich gilt 3KNF-SAT $\in$ [[NP]].
Aber vielleicht ist 3KNF-SAT einfacher als [[SAT]]?


# Eigenschaften
3KNF-SAT ist NP-vollständig.
	Wir zeigen SAT $\leq_p 3 \mathrm{KNF}$-SAT. 
	Wir geben eine [[polynomielle Reduktion]] $F \mapsto F^{\prime}$ an ( $F$ Formel, $F^{\prime}$ 3KNF-Formel) mit
	$F$ ist erfüllbar $\Leftrightarrow F^{\prime}$ ist erfüllbar
		![[Screenshot 2024-07-08 at 14.41.05.png]]



![[Screenshot 2024-07-08 at 14.50.56.png]]
