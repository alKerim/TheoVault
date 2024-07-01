Eine Menge $A\left(\subseteq \mathbb{N}\right.$ oder $\left.\Sigma^*\right)$ heißt entscheidbar gdw ihre [[charakteristische Funktion]]
$$\begin{equation*}
\chi_A(x):=\left\{\begin{array}{ll}
1 & \text { falls } x \in A \\
0 & \text { falls } x \notin A
\end{array}\right.
\end{equation*}$$
[[berechenbar]] ist.
Eine Eigenschaft/Problem $P(x)$ heißt entscheidbar gdw $\{x \mid P(x)\}$ entscheidbar ist.

# gdw's
- Eine Menge $A$ ist **entscheidbar** gdw sowohl $A$ als auch $\bar{A}$ [[semi-entscheidbar (s-e)|s-e]] sind.
	Beweis:
	"$\Rightarrow$ ": Wandle TM für $\chi_A$ in TM für $\chi_A^{\prime}$ und $\chi_{\bar{A}}^{\prime}$ um:
	![[Screenshot 2024-06-24 at 14.37.32.png|300]] ^610090
- Also wenn A s-e und $\bar{A}$ nicht-s-e, dann A [[unentscheidbar]].
	Ja gemeint sind echt semi-entscheidbare Sprachen. Also Sprachen die semi-entscheidbar aber nicht entscheidbar sind.


# Entscheidbare Probleme
- [[Wortproblem]] ist für eine [[Kontextfreie Grammatiken|CFG]] mit den [[CYK Algorithmus]] entscheidbar.
- Für eine [[Kontextfreie Grammatiken|kontextfreie Grammatik]] $G$ ist entscheidbar, ob $L(G)=\emptyset$.
![[Satz von Rice#^0f52a6]]
- Für zwei [[DPDA]] $M_1$ und $M_2$ ist $L\left(M_1\right)=L\left(M_2\right)$ entscheidbar.


# Faustregel ob entscheidbar
#theo/cheatsheet 
- Für **==[[DFA - Deterministische endliche Automaten|DFAs]]==** ist **fast ==alles== entscheidbar**:
$$$\begin{equation*}
L(A)=\emptyset, L(A)=L(B), \ldots
\end{equation*}$$
- Für **==[[Turingmaschine - TM|TMs]]==** ist **fast ==nichts== entscheidbar**:
$$\begin{equation*}$
L(M)=\emptyset, L\left(M_1\right)=L\left(M_2\right), \ldots
\end{equation*}$$
- Für **==[[Kontextfreie Grammatiken|CFGs]]==** ist **==manches== entscheidbar** $(L(G)=\emptyset, w \in L(G))$, und manches [[unentscheidbar]].



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





# Beispiele
Ist es entscheidbar, ob eine [[Turingmaschine - TM|TM]]
- mehr als 314 Zustände hat?
	ja, weil ich bei der eingabe der kodierung einfach die zustände prüfen kann
- bei Eingabe $\epsilon$ mehr als 314 Schritte macht?
	ja
- bei irgendeiner Eingabe mehr als 314 Schritte macht?
	ja, ![[Screenshot 2024-06-20 at 15.51.30.png|400]]
- bei allen Eingaben mehr als 314 Schritte macht?
- bei Eingabe $\epsilon$ ihren Kopf mehr als 314 Felder von der 0 -Position entfernen kann?
- bei Eingabe $\epsilon$ einen bestimmten Zustand erreichen kann?
- irgendeine Eingabe akzeptieren kann?



____
Related: [[nicht entscheidbar]], [[Abschlusseigenschaften Entscheidbarkeit]], [[Halteproblem]]
