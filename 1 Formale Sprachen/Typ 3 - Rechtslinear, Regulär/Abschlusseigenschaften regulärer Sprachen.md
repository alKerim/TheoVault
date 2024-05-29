Seien $R, R_1, R_2 \subseteq \Sigma^*$ [[regulär]] Sprachen. Dann sind auch
- $R_1 R_2$
- $R_1 \cup R_2$
- $R^*$
- $\bar{R}\left(:=\Sigma^* \backslash R\right)$ (Komplement)
	Komplementierung $(\bar{R})$ durch Vertauschen von Endzuständen und Nicht-Endzuständen funktioniert nur bei DFAs, nicht bei NFAs!
- $R_1 \cap R_2$
- $R_1 \backslash R_2$

reguläre Sprachen.

# Beweis
Beweis:
$R_1 R_2, R_1 \cup R_2$, und $R^*$ : klar.
$\bar{R} \quad$ Sei $R=L(A)$ für einen DFA $A=\left(Q, \Sigma, \delta, q_0, F\right)$.
Betrachte $A^{\prime}=\left(Q, \Sigma, \delta, q_0, Q \backslash F\right)$.
Dann ist $L\left(A^{\prime}\right)=\overline{L(A)}=\bar{R}$

$R_1 \cap R_2  ={R_1} \cup {R_2}$ (De Morgan)
$R_1 \backslash R_2  =R_1 \cap R_2$
