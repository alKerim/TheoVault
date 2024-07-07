
- Für jeden $\epsilon \text {-NFA } N$ gibt es einen [[NFA - Nichtdeterministische endliche Automaten|NFA]] $N^{\prime}$ mit $L(N)=L\left(N^{\prime}\right)$
	-> [[ε-NFA -> NFA]]
	Beweis:
	Seie $N=\left(Q, \Sigma, \delta, q_0, F\right)$ ein $\epsilon$-NFA. Wir definieren den NFA $N^{\prime}=\left(Q, \Sigma, \delta^{\prime}, q_0, F^{\prime}\right)$ mit folgenden Definitionen für $\delta^{\prime}$ und $F^{\prime}$ :
	$\delta^{\prime}: Q \times \Sigma \rightarrow \mathcal{P}(Q)$
$$\begin{equation*}
\delta^{\prime}(q, a):=\bigcup_{i \geq 0, j \geq 0} \hat{\delta}\left(\{q\}, \boldsymbol{\epsilon}^i a \epsilon^j\right) .
\end{equation*}$$
	Falls $N$ das leere Wort $\epsilon$ akzeptiert, also falls
$$\begin{equation*}
\exists i \geq 0 . \hat{\delta}\left(\left\{q_0\right\}, \epsilon^i\right) \cap F \neq \emptyset
\end{equation*}$$
	dann setze $F^{\prime}:=F \cup\left\{q_0\right\}$, sonst setze $F^{\prime}:=F$.


# Formale Definition
### Definition
Ein NFA mit $\epsilon$-Übergängen (auch $\epsilon$-NFA) ist ein NFA mit einem speziellen Symbol $\epsilon \notin \Sigma$ und mit
$$\begin{equation*}
\delta: Q \times(\Sigma \cup\{\boldsymbol{\epsilon}\}) \rightarrow \mathcal{P}(Q) .
\end{equation*}$$

Ein $\epsilon$-Übergang darf ausgeführt werden, ohne dass ein Eingabezeichen gelesen wird.
![[Screenshot 2024-04-28 at 19.11.04.png]]
Akzeptiert: $\epsilon, 00,11, \ldots \quad$ Nicht akzeptiert: $101, \ldots$
Bemerkung: $\epsilon \neq \epsilon ; \epsilon$ ist ein einzelnes Symbol, $\epsilon$ das leere Wort.

