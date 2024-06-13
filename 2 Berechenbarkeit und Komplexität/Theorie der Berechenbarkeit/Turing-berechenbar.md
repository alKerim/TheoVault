Eine Funktion $f: \mathbb{N}^k \rightarrow \mathbb{N}$ heißt **Turing-berechenbar** gdw es eine [[Turingmaschine - TM|Turingmaschine]] $M$ gibt, so dass für alle $n_1, \ldots n_k, m \in \mathbb{N}$ gilt
$$\begin{equation*}
\begin{array}{c}
f\left(n_1, \ldots, n_k\right)=m \Leftrightarrow \\
\exists r \in F .\left(\epsilon, q_0, \operatorname{bin}\left(n_1\right) \# b i n\left(n_2\right) \# \ldots \# b i n\left(n_k\right)\right) \\
\rightarrow_M^*(\square \ldots \square, r, \operatorname{bin}(m) \square \ldots \square)
\end{array}
\end{equation*}$$
wobei $\operatorname{bin}(n)$ die Binärdarstellung der Zahl $n$ ist.

Eine Funktion $f: \Sigma^* \rightarrow \Sigma^*$ heißt **Turing-berechenbar** gdw es eine Turingmaschine $M$ gibt, so dass für alle $u, v \in \Sigma^*$ gilt
$$\begin{equation*}
f(u)=v \quad \Leftrightarrow \quad \exists r \in F .\left(\epsilon, q_0, u\right) \rightarrow_M^*(\square \ldots \square, r, v \square \ldots \square)
\end{equation*}$$

