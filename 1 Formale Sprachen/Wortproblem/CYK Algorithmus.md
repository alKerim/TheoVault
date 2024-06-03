Der CYK-Algorithmus entscheidet das [[Wortproblem]] für [[kontextfreie Grammatiken]] in [[Chomsky-Normalform]].


# Formale Definition
Eingabe: Grammatik $G=(V, \Sigma, P, S)$ in Chomsky-Normalform, $w=a_1 \ldots a_n \in \Sigma^*$

Wir definieren:
$V_{i j}:=\left\{A \in V \mid A \rightarrow{ }_G^* a_i \ldots a_j\right\} \quad \text { für } i \leq j$
Damit gilt:
$w \in L(G) \quad \Leftrightarrow \quad S \in V_{1 n}$


# Zeit
#theo/zeit
Der CYK-Algorithmus entscheidet das Wortproblem $w \in L(G)$ für eine fixe CFG G in Chomsky-Normalform in Zeit 
$O\left(|w|^3\right)$ !!!!!! (Abhängig von Wortlänge)


# Bedeutung der Indizes
Gegeben sei ein Wort $w=x_1x_2x_3x_4x_5$ der Länge fünf Symbole.
Im CYK Algorithmus bedeutet der Indiz des Feldes 1,3 für das Wort $w$, ob das Teilwort $x_1x_2x_3$ der ersten 3 Symbolen in $w$ in der Sprache $L$ enthalten ist.
Das gleiche gilt für 2,5 für die Symbole zwei bis fünf, also ob $x_2x_3x_4x_5$ enthalten ist.
