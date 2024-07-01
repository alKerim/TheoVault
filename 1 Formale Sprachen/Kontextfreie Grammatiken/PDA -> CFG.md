Zu jedem PDA $M=\left(Q, \Sigma, \Gamma, q_0, Z_0, \delta\right)$, der mit leerem Keller akzeptiert, kann man eine CFG $G$ konstruieren mit $L(G)=L_\epsilon(M)$.

Konstruktion: $G:=(V, \Sigma, P, S)$ mit
$V:=Q \times \Gamma \times Q \cup\{S\} \quad$ wobei wir die Tripel mit [.,.,.] notieren und $P$ die folgenden Produktionen enthält:
- $S \rightarrow\left[q_0, Z_0, q\right]$ für alle $q \in Q$
- Für alle $\delta(q, b, Z) \ni\left(r_0, Z_1 \ldots Z_k\right)$ und für alle $r_1, \ldots, r_k \in Q$ ([[Kellerautomat - PDA#^b4c8c3|siehe formale transition in pda]]):
$$\begin{equation*}
\left[q, Z, r_k\right] \rightarrow b\left[r_0, Z_1, r_1\right]\left[r_1, Z_2, r_2\right] \ldots\left[r_{k-1}, Z_k, r_k\right]
\end{equation*}$$

Idee: $\left[q, Z, r_k\right] \rightarrow_G^* w \operatorname{gdw}(q, w, Z) \rightarrow_M^*\left(r_k, \epsilon, \epsilon\right)$
Die $r_1, \ldots, r_k$ sind potenzielle Zwischenzustände beim Akzeptieren der Teilwörter von $b u_1 \ldots u_k=w$, die zu $Z_1, \ldots, Z_k$ gehören. (Zerlegungssatz!)

____
$[q, Z, p] \rightarrow_G^n w \operatorname{gdw}(q, w, Z) \rightarrow_M^n(p, \epsilon, \epsilon)$
