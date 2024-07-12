Anfang Formalitäten wie bei [[Konstruktion einer Grammatik]], bloß mit dem Tupel eines [[Kellerautomat - PDA|PDA]].

Tupel:
$M=\left(Q, \Sigma, \Gamma, q_0, Z_0, \delta, F\right)$ 

# Beispiel
### Aufgabenstellung
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


