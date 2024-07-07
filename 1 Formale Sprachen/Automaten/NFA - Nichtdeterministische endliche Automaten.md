NFA sind eine Verallgemeinerung von [[DFA - Deterministische endliche Automaten|DFA]]: Aus einem Zustand kann es 0, 1, 2, ... Übergänge mit derselben Beschriftung geben.

# Fakten
- Jeder DFA ist ein NFA
- Wort wird akzeptiert gdw mindestens eine dieser Zustandsfolgen zu einem Endzustand führt.
	Intuition: Automat "rät" den richtigen Weg
- NFA sind ==nicht== nützlich als [[Recognizer]], aber ==als Zwischenschritt== oder Datenstruktur #theo/wichtig 


# Formale Definition
### Definition
#theo/basics
Ein nichtdeterministischer endlicher Automat (nondeterministic finite automaton, NFA) ist ein 5-Tupel $N=\left(Q, \Sigma, \delta, q_0, F\right)$, so dass
- $Q, \Sigma, q_0$ und $F$ sind wie bei einem DFA
- $\delta: Q \times \Sigma \rightarrow \mathcal{P}(Q)$
$\mathcal{P}(Q)=$ Menge aller Teilmengen von $Q=2^Q$.
($\mathcal{P}(Q)$ steht für Potenzmenge von $Q$ )
Alternative: Relation $\delta \subseteq Q \times \Sigma \times Q$.

### $\hat{\bar{\delta}}$ vs. $\hat{\delta}$
$\hat{\bar{\delta}}(S, w)$ ist **Menge aller Zustände** die sich von einem Zustand in $S$ aus mit $w$ erreichen lassen.
	im Vergleich $\hat{\bar{\delta}}$ ist im DFA:![[DFA - Deterministische endliche Automaten#^cefbf7]]
#### Vereinfachte Schreibweise in Praxis
Oft schreiben wir nur $\delta$ statt $\bar{\delta}$ und $\hat{\delta}$ statt $\hat{\delta}$ (vgl. overloading in Programmiersprachen).


# Beispiel
![[Screenshot 2024-04-28 at 16.09.19.png|350]] $\begin{array}{c|c|c|} \delta & 0 & 1 \\ \hline p & \{p\} & \{p, q\} \\ \hline q & \{r\} & \{r\} \\ \hline r & \emptyset & \emptyset \\ \hline \end{array}$


$$\begin{equation*}
\begin{array}{ll}
\text { Erweiterung } & \text { von } \delta: \quad Q \times \Sigma \rightarrow \mathcal{P}(Q) \\
& \text { auf } \bar{\delta}: \mathcal{P}(Q) \times \Sigma \rightarrow \mathcal{P}(Q) \text { definiert durch } \\
& \bar{\delta}(S, a):=\bigcup_{q \in S} \delta(q, a) \\
\text { Es folgt: } & \hat{\bar{\delta}}: \mathcal{P}(Q) \times \Sigma^* \rightarrow \mathcal{P}(Q)
\end{array}
\end{equation*}
$$
Intuition: 
$\hat{\delta}(S, w)$ ist Menge aller Zustände die sich von einem Zustand in $S$ aus mit $w$ erreichen lassen.

Die von $N=\left(Q, \Sigma, \delta, q_0, F\right)$ akzeptierte Sprache ist

$L(N):=\left\{w \in \Sigma^* \mid \hat{\bar{\delta}}\left(\left\{q_0\right\}, w\right) \cap F \neq \emptyset\right\}$ ^c07332


Oft schreiben wir nur $\delta$ statt $\bar{\delta}$ und $\hat{\delta}$ statt $\hat{\delta}$ (vgl. overloading in Programmiersprachen).