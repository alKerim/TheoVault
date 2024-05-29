#theo/algorithmus

# Algorithmus
Eingabe: Eine kontextfreie Grammatik $G=(V, \Sigma, P, S)$

**(1)** Füge für jedes $a \in \Sigma$, das in einer rechten Seite der Länge $\geq 2$ vorkommt, ein neues Nichtterminal $A_a$ zu $V$ hinzu, ersetze $a$ in allen rechten Seiten der Länge $\geq 2$ durch $A_a$, und füge $A_a \rightarrow a$ zu $P$ hinzu.

**(2)** Ersetze jede Produktion der Form
	$A \rightarrow B_1 B_2 \cdots B_k(k \geq 3)$
durch
	$A \rightarrow B_1 C_2, C_2 \rightarrow B_2 C_3, \ldots, C_{k-1} \rightarrow B_{k-1} B_k$

wobei $C_2, \ldots, C_{k-1}$ neue Nichtterminale sind.

**(3)** Eliminiere alle $\epsilon$-Produktionen.

**(4)** Eliminiere alle Kettenproduktionen.
	[[Chomsky-Normalform#Beispiel 1 Loop finding Trick|Ketten-Trick]]



