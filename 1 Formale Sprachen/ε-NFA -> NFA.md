[[theo-folien-handout.pdf#page=51|Lemma 3.16]]
Für jeden $\epsilon$-NFA $N$ gibt es einen NFA $N^{\prime}$ mit $L(N)=L\left(N^{\prime}\right)$.

# Konstruktion
Seie $N=\left(Q, \Sigma, \delta, q_0, F\right)$ ein $\boldsymbol{\epsilon}$-NFA. Wir definieren den NFA $N^{\prime}=\left(Q, \Sigma, \delta^{\prime}, q_0, F^{\prime}\right)$ mit folgenden Definitionen für $\delta^{\prime}$ und $F^{\prime}$ :
- $\delta^{\prime}: Q \times \Sigma \rightarrow \mathcal{P}(Q)$
$$\begin{equation*}
\delta^{\prime}(q, a):=\bigcup_{i \geq 0, j \geq 0} \hat{\delta}\left(\{q\}, \epsilon^i a \epsilon^j\right) .
\end{equation*}$$
- Falls $N$ das leere Wort $\epsilon$ akzeptiert, also falls
$$\begin{equation*}
\exists i \geq 0 . \hat{\delta}\left(\left\{q_0\right\}, \epsilon^i\right) \cap F \neq \emptyset
\end{equation*}$$
dann setze $F^{\prime}:=F \cup\left\{q_0\right\}$, sonst setze $F^{\prime}:=F$.

