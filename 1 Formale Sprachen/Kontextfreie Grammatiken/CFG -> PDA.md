Zu jeder [[Kontextfreie Grammatiken|CFG]] G kann man einen PDA $M$ konstruieren, der mit leerem Stack akzeptiert, so dass $L_\epsilon(M)=L(G)$.

Konstruktion:
Zuerst bringen wir alle Produktionen von $G$ in die Form
$$\begin{equation*}
A \rightarrow b B_1 \ldots B_k
\end{equation*}$$
wobei $b \in \Sigma \cup\{\epsilon\}$.
Methode: Für jedes $a \in \Sigma$
(1) füge ein neues $A_a$ zu $V$ hinzu,
(2) ersetze $a$ rechts in $P$ durch $A_a$ (außer am Kopfende),
(3) füge eine neue Produktion $A_a \rightarrow a$ hinzu.

Alle Produktionen in $G=(V, \Sigma, P, S)$ haben jetzt die Form
$A \rightarrow b B_1 \ldots B_k$

Der PDA wird wie folgt definiert:
$M \quad:=\quad(\{q\}, \Sigma, V, q, S, \delta)$

wobei
$(A \rightarrow b \beta) \in P \Longrightarrow \delta(q, b, A) \ni(q, \beta)$

also für alle $b \in \Sigma \cup\{\epsilon\}$ und $A \in V$ :
$\delta(q, b, A):=\{(q, \beta) \mid(A \rightarrow b \beta) \in P\}$


