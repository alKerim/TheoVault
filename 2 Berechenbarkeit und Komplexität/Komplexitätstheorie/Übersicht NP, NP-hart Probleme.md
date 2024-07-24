
| $\in$ P                                                                                                               | $\in$ NP und nicht NP-voll | $\in$ NP-vollständig | $\in$ NP-hart $\cap \notin$ NP |
| --------------------------------------------------------------------------------------------------------------------- | -------------------------- | -------------------- | ------------------------------ |
| Sortieren von Listen                                                                                                  | reguläre Sprachen          | SAT                  | H (alle Halteprobleme)         |
| 2KNF-SAT                                                                                                              |                            | 3KNF-SAT             | PCP                            |
| $\left\{w w^R \mid w \in \Sigma^*\right\} \in \operatorname{TIME}\left(O\left(n^2\right)\right) \subseteq \mathrm{P}$ |                            | MÜ                   | Äquivalenz-problem für CFGs    |
| $\{(G, w) \mid G$ ist CFG $\wedge w \in L(G)\} \in \mathrm{P}$                                                        |                            | CLIQUE               |                                |
| $\{(G, w) \mid G$ ist Graph $\wedge w$ ist Pfad in $G\} \in \mathrm{P}$                                               |                            | RUCKSACK             |                                |
| $\{b i n(p) \mid p$ Primzahl $\} \in \mathrm{P}$                                                                      |                            | PARTITION            |                                |
| 2COL                                                                                                                  |                            | TSP                  |                                |
|                                                                                                                       |                            | kCOL für $k \geq 3$  |                                |
|                                                                                                                       |                            | HAMILTON             |                                |

# WICHTIGE NP Regeln
- $A \leq_p B$ genau dann wenn $\bar{A} \leq_p \bar{B}$.
- Sei $H$ das (allgemeine) Halteproblem. Wenn $A \in N P$, dann $A \leq_p H$.

# NP aufgaben
Sei $\Sigma:=\{a, b\}$ und sei $L \subseteq \Sigma^*$. Welche der folgenden Aussagen sind wahr?
- Wenn $L^a \in N P$ und $L^b \in N P$, dann ist $L \in N P$.
- Wenn $L \in N P$, dann ist $L^a \in N P$.
- NICHT: Wenn $L^a \in N P$, dann ist $L \in N P$.

Sei $\Sigma$ ein Alphabet. Sei $\mathcal{K}$ die Menge aller kontextfreien Grammatiken mit Terminalen aus $\Sigma$. Gegeben eine Sprache $L \subseteq \Sigma^*$, sei $\min (L)$ die Menge der kürzesten Wörter in $L$. Welche der folgenden Mengen sind entscheidbar?
- [ ] yes: $\left\{\left(G_1, G_2\right) \in \mathcal{K} \times \mathcal{K} \mid \min \left(L\left(G_1\right)\right) \subseteq L\left(G_2\right)\right\}$
- [ ] no: $\left\{\left(G_1, G_2\right) \in \mathcal{K} \times \mathcal{K} \mid L\left(G_1\right) \backslash \min \left(L\left(G_1\right)\right)=L\left(G_2\right)\right\}$
- [ ] no: $\left\{\left(G_1, G_2\right) \in \mathcal{K} \times \mathcal{K} \mid L\left(G_1\right) \backslash L\left(G_2\right)=\emptyset\right\}$

