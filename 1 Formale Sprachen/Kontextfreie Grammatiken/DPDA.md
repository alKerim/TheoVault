Deterministischer Kellerautomat (deterministic pushdown automaton)

- Erkennt [[DCFL]]s
- Jeden kann man [[DFA - Deterministische endliche Automaten|DFA]] leicht mit einem [[DPDA]] simulieren.

Ein [[Kellerautomat - PDA|PDA]] heißt [[Determinismus|deterministisch]] (DPDA) gdw für alle $q \in Q, a \in \Sigma$ und $Z \in \Gamma$
$|\delta(q, a, Z)|+|\delta(q, \epsilon, Z)| \leq 1$



# Beispiele
#### Beispiel 1
Der folgende DPDA mit $\Sigma=\{0,1, \$\}, \Gamma=\left\{Z_0, 0,1\right\}$ akzeptiert die Sprache $\left\{w \$ w^R \mid w \in\{0,1\}^*\right\}$.