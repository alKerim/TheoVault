Eine Grammatik ist ein 4-Tupel $G=(V, \Sigma, P, S)$.

Wir haben meistens eine Grammatik $G$ gegeben und müssen daraus eine Grammatik $G'$ konstruieren.
Dabei müssen wir festlegen: $G'=(V',\Sigma',P',S')$
In 99% der Fälle ist $\Sigma'=\Sigma$. 
Die restlichen $V',P',S'$ müssen wir alle manuell selber definieren.


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
