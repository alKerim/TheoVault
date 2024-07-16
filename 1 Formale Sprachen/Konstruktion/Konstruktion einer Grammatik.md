Eine Grammatik ist ein 4-Tupel $G=(V, \Sigma, P, S)$.

Wir haben meistens eine Grammatik $G$ gegeben und müssen daraus eine Grammatik $G'$ konstruieren.
Dabei müssen wir festlegen: $G'=(V',\Sigma',P',S')$
In 99% der Fälle ist $\Sigma'=\Sigma$. 
Die restlichen $V',P',S'$ müssen wir alle manuell selber definieren.


# o.B.d.A
Kann man benutzen um sicherzustellen, dass Symbole anders benannt sind:
- $V_{1}\cap V_{2}= \emptyset$ 
- $S \not \in V_{1}\cup V_2$ (neues Startsymbol ist weder in $V_1$ noch in $V_2$)



# Beispiele für Cheatsheet
#theo/cheatsheet 
### Grammatik konstruieren
Beispiele von [HA5.6 a) und b)](https://teaching.model.in.tum.de/2024ss/theo/ex/ha06-solution.pdf?key=DOuuxWLm)
Sei $\Sigma:=\{a, b\}$ und $L \subseteq \Sigma^{+}$eine kontextfreie Sprache. Konstruieren Sie eine kontextfreie Grammatik $G^{\prime}$ für die Sprachen
(a) $L^a$
	$V'= V \cup \{X_{a}| X \in V\}$ 
	Für $(X \rightarrow a) \in P$ fügen wir $X_a \rightarrow \varepsilon$ zu $P^{\prime}$ hinzu.
	Für $(X \rightarrow Y Z) \in P$ fügen wir $X_a \rightarrow Y_a Z$ zu $P^{\prime}$ hinzu.
	$S' = S_a$ 
(b) $\{w \in L:|w| \equiv 0(\bmod 7)\}$
	$V^{\prime}:=\left\{X_i: X \in V, i \in\{0, \ldots, 6\}\right\}$ 
	Die Idee ist, dass $L_{G^{\prime}}\left(X_i\right)=\left\{w \in L_G(X):|w| \equiv i(\bmod 7)\right\}$ gilt
	Also $X_i$ genau die Wörter erzeugt, die $X$ erzeugt und deren Länge geteilt durch 7 Rest $i$ hat. 
	- Für $(X \rightarrow a) \in P$ fügen wir $X_1 \rightarrow a$ zu $P^{\prime}$ hinzu.
	- Für $(X \rightarrow Y Z) \in P$ fügen wir $X_i \rightarrow Y_j Z_k$ zu $P^{\prime}$ hinzu, für alle $i, j, k \in\{0, \ldots, 6\}$ $\operatorname{mit} i \equiv j+k(\bmod 7)$
	$S^{\prime}:=S_0$. 


### CFG $\cap$ DFA
Beispiel von [HA7.2](https://teaching.model.in.tum.de/2024ss/theo/ex/ha07-solution.pdf?key=jq5e9s7L)
Gegeben: 
- $\Sigma:=\{a, b\}$, 
- $G=(V, \Sigma, P, S)$ eine CFG in CNF, 
- DFA $M=$ $\left(Q, \Sigma, \delta, q_0, F\right)$ ein DFA. 
Gesucht:
- Konstruktion von CFG $G^{\prime}=\left(V^{\prime}, \Sigma, P^{\prime}, S^{\prime}\right)$ für $L(G') = L(G) \cap L(M)$ erzeugen, und damit beweisen, dass die kontextfreien Sprachen abgeschlossen unter Schnitt mit regulären Sprachen sind.
- Konstruieren Sie $G^{\prime}$. Geben Sie also insbesondere die Produktionen $P^{\prime}$ an.
- Hinweis: $G^{\prime}$ muss nicht in CNF sein.

Lösung: 
- $V^{\prime}:=\left\{S^{\prime}\right\} \cup\left\{X_{q, r}: X \in V, q, r \in Q\right\}$. 
- Die Idee ist, dass $X_{q, r}$ genau die Wörter erzeugt, die sowohl von $X$ erzeugt werden können, als auch im DFA von Zustand $q$ nach $r$ gehen. 
	- Formal soll also $L_{G^{\prime}}\left(X_{q, r}\right)=\left\{w \in L_G(X): \hat{\delta}(q, w)=\right.$ $r\}$ gelten. 
	- Zusätzlich ist $S^{\prime}$ ein besonderes Startsymbol.
- $P'$:
	- $S^{\prime} \rightarrow S_{q_0, r}$ für alle $r \in F$,
	- $X_{q, r} \rightarrow Y_{q, s} Z_{s, r}$ für alle $(X \rightarrow Y Z) \in P$ und $q, s, r \in Q$, und
	- $X_{q, r} \rightarrow c$ für alle $(X \rightarrow c) \in P$, falls $\delta(q, c)=r$.
- Startsymbol ist oben schon auf $S'$ festgelegt


### L(H) = L(G)L(G) mit H einer Typ-0 Grammatik
[HA8.3 b) = Endterm23 Aufgabe](https://teaching.model.in.tum.de/2024ss/theo/ex/ha08-nosolution.pdf?key=zgUXbnR5)
Erinnerung: Eine Grammatik vom Typ 0 kann sowohl Terminale als auch Nichtterminale auf beiden Seiten ihrer Produktionen besitzen, d.h. $P \subseteq(V \cup \Sigma)^* \times(V \cup \Sigma)^*$.

Geben Sie ein Verfahren an, das als Input eine Grammatik $G=(V, \Sigma, P, S)$ erhält und eine Grammatik $H$ mit $L(H)=L(G) L(G)$ und höchstens $3(|\Sigma|+|P|)$ Produktionen konstruiert. Erläutern Sie die Idee Ihres Verfahrens auch informell.

#### Lösung
Wir definieren zwei disjunkte Kopien von $G$ namens $G'$, $G''$ für die gelten soll, dass $L(G')=L(G'')=L(G)$

$G^{\prime}=\text { wobei }\left(V^{\prime}, \Sigma, P^{\prime}, S^{\prime}\right)$, $G^{\prime\prime}=\text { wobei }\left(V^{\prime\prime}, \Sigma, P^{\prime\prime}, S^{\prime\prime}\right)$
$V^{\prime}=\left\{X^{\prime} \mid \forall X \in V\right\} \cup\left\{x^{\prime} \mid x \in \Sigma\right\}$, $V^{\prime\prime}=\left\{X^{\prime\prime} \mid \forall X \in V\right\} \cup\left\{x^{\prime\prime} \mid x \in \Sigma\right\}$
$P'$:
- $\left\{X_1^{\prime} \ldots X_n^{\prime} \rightarrow Y_1^{\prime} \ldots Y_m^{\prime} \mid \forall i, j \in \mathbb{N} . i \leq n \cap j \leq m \cap \left\{x_1 \ldots x_n \rightarrow Y_1 \ldots Y_m\right\} \in P \cap X_i \in(g \vee \cup \Sigma) \wedge Y_s \in(\vee \cup \Sigma) \right\}$
- $S^{\prime}=S^{\prime} \in V^{\prime}$
$P''$:
- $\left\{X_1^{\prime\prime} \ldots X_n^{\prime\prime} \rightarrow Y_1^{\prime\prime} \ldots Y_m^{\prime\prime} \mid \forall i, j \in \mathbb{N} . i \leq n \cap j \leq m \cap \left\{x_1 \ldots x_n \rightarrow Y_1 \ldots Y_m\right\} \in P \cap X_i \in(g \vee \cup \Sigma) \wedge Y_s \in(\vee \cup \Sigma) \right\}$- $S^{\prime\prime}=S^{\prime\prime} \in V^{\prime\prime}$

Nun spezifizieren wir Grammatik $H$.
Wie oben bereits angegeben ist $H=\left(V^H, \Sigma, P^H, S^H\right)$
$V^H=V^{\prime} \cup V^{\prime\prime} \cup\left\{S^H\right\}$
$P^H=P^{\prime} \cup P^{\prime\prime} \cup\left\{S^H \rightarrow S^{\prime} S^{\prime\prime}\right\}$

Für die Anzahl an Produktionen in $H$ gilt:
$$\begin{equation*}
\begin{aligned}
\left|P^{H}\right| & =|P^{\prime}|+\left|P^{\prime\prime}\right|+1 \\
& =|P|+(|P|+|\Sigma|)+1 \\
& =2 \cdot|P|+|\Sigma|+1 \leq 3 \cdot(|\Sigma|+|P|)
\end{aligned}
\end{equation*}$$

Nun gilt $L(H)=L(G^{\prime}) L\left(G^{\prime\prime}\right)=L(G) L(G)$


