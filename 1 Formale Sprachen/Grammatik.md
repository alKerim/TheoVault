Eine Grammatik ist ein 4-Tupel $G=(V, \Sigma, P, S)$, wobei
- $V$ ist eine endliche Menge von Nichtterminalzeichen (oder Nichtterminale, oder Variablen),
- $\Sigma$ ist eine endliche Menge von Terminalzeichen (oder Terminale), disjunkt von $V$, auch genannt ein Alphabet,
- $P \subseteq(V \cup \Sigma)^* \times(V \cup \Sigma)^*$ ist eine Menge von Produktionen, und 
- $S \in V$ ist das Startsymbol.
_______
Die von $M$ akzeptierte Sprache ist
$$\begin{equation*}
L(M):=\left\{w \in \Sigma^* \mid \hat{\delta}\left(q_0, w\right) \in F\right\},
\end{equation*}$$
wobei $\hat{\delta}: Q \times \Sigma^* \rightarrow Q$ induktiv definiert ist durch
$$\begin{equation*}
\begin{aligned}
\hat{\delta}(q, \epsilon) & =q \\
\hat{\delta}(q, a w) & =\hat{\delta}(\delta(q, a), w) \quad \text { für } a \in \Sigma, w \in \Sigma^* .
\end{aligned}
\end{equation*}$$
( $\hat{\delta}(q, w)$ bezeichnet den Zustand, den man aus $q$ mit $w$ erreicht. )



# Notation basic wichtig
$L(G)$ ist die [[Sprache]] die von der Grammatik $G$ beschrieben wird.

# Beispielgrammatik:
![[Screenshot 2024-04-26 at 15.23.39.png]]

# Konventionen:
- $A, B, C, \ldots$ sind Nichtterminale,
- $a, b, c, \ldots$ (und Sonderzeichen wie $+, *, \ldots$ ) sind Terminale,
- $\alpha, \beta, \gamma, \ldots \in(V \cup \Sigma)^*$
- Produktionen schreiben wir $\alpha \rightarrow \beta$ statt $(\alpha, \beta) \in P$.
- Statt $\alpha \rightarrow \beta_1, \ldots, \alpha \rightarrow \beta_n$ schreiben wir $\alpha \rightarrow \beta_1|\cdots| \beta_n$

# Ableitung eines Wortes in einer Grammatik
Man kann zeigen wie ein Wort mit einer Grammatik erzeugt wurde, indem man die **Ableitungsrelation** benutzt. 
Somit kann man sukzessiv zeigen wie ein Wort produziert wurde durch eine **Ableitung**.

Formal:
Eine Sequenz $\alpha_1 \rightarrow_G \alpha_2 \rightarrow_G \cdots \rightarrow_G \alpha_n$ ist eine Ableitung von $\alpha_n$ aus $\alpha_1$.
Wenn $\alpha_1=S$ und $\alpha_n \in \Sigma^*$, dann erzeugt $G$ das Wort $\alpha_n$.
Die [[Sprache]] von $G$ ist die Menge aller Wörter, die von $G$ erzeugt werden. Sie wird mit $L(G)$ bezeichnet.

![[Screenshot 2024-04-26 at 15.25.05.png]]
