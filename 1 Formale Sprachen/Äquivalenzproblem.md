#theo/probleme 
Sei $G_1,G_2$ ein DFA, NFA, RE, rechtslineare Grammatik ....

Gegeben $G_1, G_2$, gilt $L\left(G_1\right)=L\left(G_2\right)$ ? ^06dfa8

### Entscheidbarkeit
Das Äquivalenzproblem ist für DFAs [[entscheidbar]].
Das Äquivalenzproblem für reguläre Ausdrücke ist [[entscheidbar]].


### Beweis
Folgt direkt aus
$$\begin{equation*}
\begin{array}{l}
L_1 \subseteq L_2 \quad \Leftrightarrow \quad L_1 \cap \overline{L_2}=\emptyset \\
L_1=L_2 \quad \Leftrightarrow \quad L_1 \subseteq L_2 \wedge L_2 \subseteq L_1
\end{array}
\end{equation*}$$
da für DFAs Komplement und Durchschnitt wieder endliche Automaten liefern und das [[Leerheitsproblem]] für endliche Automaten entscheidbar ist.


### Laufzeit DFA
Das Äquivalenzproblem für DFAs ist in Zeit 
$O\left(\left|Q_1\right|\left|Q_2\right||\Sigma|\right)$ 
entscheidbar.

Beweis:
Geg.: DFAs $M_1$ mit $m$ und $M_2$ mit $n$ Zuständen. Mit Hilfe der [[DFA + DFA (Produkt-konstruktion)|Produkt-Konstruktion]] für $\cap$ folgt:
$$\begin{array}{c|c} 
& \text { Anzahl der Zustände } \\
\hline L\left(M_1\right) \cap \overline{L\left(M_2\right)} & m n \\
\overline{L\left(M_1\right)} \cap L\left(M_2\right) & m n
\end{array}$$


### Laufzeit NFA
Das Äquivalenzproblem für NFAs ist in Zeit 
$O\left(2^{\left|Q_1\right|+\left|Q_2\right|}\right)$
entscheidbar (bei fixem $\Sigma$ ).

Beweis:
2 NFAs mit $m$ und $n$ Zuständen $\rightsquigarrow$
2 DFAs mit $2^m$ und $2^n$ Zuständen
Äquivalenztest in Zeit $O\left(2^m 2^n\right)$
