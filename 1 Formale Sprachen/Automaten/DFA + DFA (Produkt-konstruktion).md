Beide DFAs laufen synchron parallel, ==Wort wird akzeptiert wenn beide akzeptieren==.

Parallelismus = Kreuzprodukt der Zustandsräume
-> TODO: was bedeutet das ?


Sprache A, Sprache B
A,B Produkt-konstruktion = $A \cap B$



# Formale Definition
Sind $M_1=\left(Q_1, \Sigma, \delta_1, s_1, F_1\right)$ und $M_2=\left(Q_2, \Sigma, \delta_2, s_2, F_2\right) D F A$, dann ist der Produkt-Automat
$$\begin{equation*}
\begin{array}{c}
M:=\left(Q_1 \times Q_2, \Sigma, \delta,\left(s_1, s_2\right), F_1 \times F_2\right) \\
\delta\left(\left(q_1, q_2\right), a\right):=\left(\delta_1\left(q_1, a\right), \delta_2\left(q_2, a\right)\right)
\end{array}
\end{equation*}$$
$L\left(M_1\right) \cap L\left(M_2\right)= (Q_1 \times F_{2} )\cup (Q_2 \times F_{1} )$


ein DFA der $L\left(M_1\right) \cap L\left(M_2\right)$ akzeptiert.
Erinnerung: $\left|Q_1 \times Q_2\right|=\left|Q_1\right|\left|Q_2\right|$.

