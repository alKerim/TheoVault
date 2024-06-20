Eine Funktion $f: \mathbb{N}^k \rightarrow \mathbb{N}$ ist **intuitiv berechenbar**, wenn es einen Algorithmus gibt, der bei Eingabe $\left(n_1, \ldots, n_k\right) \in \mathbb{N}^k$
- nach endlich vielen Schritten mit Ergebnis $f\left(n_1, \ldots, n_k\right)$ hält, falls $f\left(n_1, \ldots, n_k\right)$ definiert ist,
- und nicht terminiert, falls $f\left(n_1, \ldots, n_k\right)$ nicht definiert ist.

Was bedeutet „Algorithmus“? Assembler? C? Java? OCaml? Macht es einen Unterschied?


# Anders formuliert
$f$ it intuitiv berechenbar gdw. es eine Menge vor Programmen $M=\left\{P_1, P_2, P_3, \ldots\right\}$ gibt, sodass as ein i gibt mit $P_i(x)=f(x)$ für alle $x$.

Wichtig: Jedes P_i muss eine endliche Länge haben aber M darf unendlich oder überzahlbar sien.



# Beispiele
- Denke an eine bel.rationale Zahl n $f_3=$ 1 falls x=n, sonst 0
	Berechenbar, weil wir rationale Zahlen per definition in endlich vielen bruchen darstellen konnen, und deshalb wie mit f_1 prüfen konnen
