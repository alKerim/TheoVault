
# Entscheidbare Probleme
- [[Wortproblem]] ist für eine [[Kontextfreie Grammatiken|CFG]] mit den [[CYK Algorithmus]] entscheidbar.
- Für eine [[Kontextfreie Grammatiken|kontextfreie Grammatik]] $G$ ist entscheidbar, ob $L(G)=\emptyset$.




# Zeit
Entscheidbarkeit
$$\begin{array}{l}
\text { Entscheidbarkeit }\\
\begin{array}{|l|c|c|c|c|}
\hline & \text { Wortproblem } & \text { Leerheit } & \text { Äquivalenz } & \text { Schnittproblem } \\
\hline \text { DFA } & O(n) & \text { ja } & \text { ja } & \text { ja } \\
\hline \text { DPDA } & O(n) & \text { ja } & \text { ja } & \text { nein } \left.*^*\right) \\
\hline \text { CFG } & O\left(n^3\right) & \text { ja } & \text { nein }\left({ }^*\right) & \text { nein(*) } \\
\hline
\end{array}
\end{array}$$


____
Related: [[nicht entscheidbar]]