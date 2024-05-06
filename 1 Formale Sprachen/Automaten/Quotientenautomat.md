Die „[[Kollabierter Automat|Kollabierung]]“ von $M$ bzgl. $\equiv$ ist der Quotientenautomat:

Definition 3.54 (Quotientenautomat)
$$\begin{equation*}
\begin{aligned}
M / \equiv & :=\left(Q / \equiv, \Sigma, \delta^{\prime},\left[q_0\right]_{\equiv}, F / \equiv\right) \\
\delta^{\prime}\left([p]_{\equiv}, a\right) & :=[\delta(p, a)]_{\equiv}
\end{aligned}
\end{equation*}$$

Die Definition von $\delta^{\prime}$ ist wohlgeformt da unabhängig von der Wahl des Repräsentanten $p$ :
$$\begin{equation*}
\begin{array}{l}
{[p]_{\equiv}=\left[p^{\prime}\right]_{\equiv} \Longrightarrow p \equiv p^{\prime} \Longrightarrow \delta(p, a) \equiv \delta\left(p^{\prime}, a\right)} \\
\Longrightarrow[\delta(p, a)]_{\equiv}=\left[\delta\left(p^{\prime}, a\right)\right]_{\equiv} \\
\end{array}
\end{equation*}$$


$M$ und $M / \equiv$ erkennen die gleiche Sprache: $L(M / \equiv)=L(M)$.

Beweis: Übung.

## Minimalität des Quotientenautomaten:
![[Residualsprache]]

![[Äquivalenz von Wörtern bzgl. L]]
