Eine Turingmaschine (TM) ist ein 7-Tupel $M=\left(Q, \Sigma, \Gamma, \delta, q_0, \square, F\right)$ so dass
- $Q$ ist eine endliche Menge von Zuständen.
- $\Sigma$ ist eine endliche Menge, das Eingabealphabet.
- $\Gamma$ ist eine endliche Menge, das Bandalphabet, mit $\Sigma \subset \Gamma$
- $\delta: Q \times \Gamma \rightarrow Q \times \Gamma \times\{L, R, N\}$ ist die Übergangsfunktion. $\delta$ darf partiell sein.
- $q_0 \in Q$ ist der Startzustand.
- $\square \in \Gamma \backslash \Sigma$ ist das Leerzeichen.
- $F \subseteq Q$ ist die Menge der akzeptierenden oder Endzustände.

- Annahme: $\delta(q, a)$ is nicht definiert für alle $q \in F$ und $a \in \Gamma$.
- Eine [[Nichtdeterminismus|nichtdeterministische]] Turingmaschine hat eine Übergangsfunktion $\delta: Q \times \Gamma \rightarrow \mathcal{P}(Q \times \Gamma \times\{L, R, N\})$.

![[Screenshot 2024-06-13 at 14.52.58.png|400]]

# Konfigurationen
Eine Konfiguration einer Turingmaschine ist ein Tripel
$$\begin{equation*}
(\alpha, q, \beta) \in \Gamma^* \times Q \times \Gamma^* \text {. }
\end{equation*}$$
Dies modelliert
- Bandinhalt: ... $\square \alpha \beta \square \ldots$
- Zustand: $q$
- Kopf auf dem ersten Zeichen von $\beta \square$

#### Startkonfiguration
Die Startkonfiguration der Turingmaschine bei Eingabe $w \in \Sigma^*$ ist $\left(\epsilon, q_0, w\right)$.

#### intuitiv
Intuitiv bedeutet $\quad \delta(q, a)=\left(q^{\prime}, b, D\right)$ :
- Wenn sich $M$ im Zustand $q$ befindet,
- und auf dem Band $a$ liest,
- so geht $M$ im nächsten Schritt in den Zustand $q^{\prime}$ über,
- überschreibt $a$ mit $b$,
- und bewegt danach den Schreib-/Lesekopf nach rechts (falls $D=R$ ), nach links (falls $D=L$ ), oder nicht (falls $D=N$ ).



# TM akzeptiert
Eine Turingmaschine $M$ akzeptiert die Sprache
$$\begin{equation*}
L(M)=\left\{w \in \Sigma^* \mid \exists q \in F, \alpha, \beta \in \Gamma^* .\left(\epsilon, q_0, w\right) \rightarrow_M^*(\alpha, q, \beta)\right\}
\end{equation*}$$

![[Turing-berechenbar]]

