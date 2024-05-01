
Für jeden DFA $M$ gibt es eine rechtslineare Grammatik $G$ mit $L(M)=L(G)$.


# Vorgehen
TODO: aus Vorlesung noch eintragen:


### Schritt 1 (Nicht-Terminale definieren)
1. Zustände werden umbenannt in Großbuchstaben, 
2. Jeder Zustand wird jetzt interpretiert als Nicht-Terminal
3. Also $\forall$ Zustand = Nicht-Terminal


### Schritt 2 (Übergänge)
Jeder Übergang wird nun einzeln betrachtet, also zB. Übergang S ---a---> B
ist nun grammatische Regel: (S->aB)

==Wichtige Regel: Nur das Startsymbol darf eine Produktion zu $\epsilon$ haben.
(Im Praxis nicht so oft)==



# Beweis
Sei $M=\left(Q, \Sigma, \delta, q_0, F\right)$. Die Grammatik $G=(V, T, P, S)$ mit
- $V=Q, T=\Sigma, S=q_0$,
- $\left(q_1 \rightarrow a q_2\right) \in P \operatorname{gdw} \delta\left(q_1, a\right)=q_2$,
- $\left(q_1 \rightarrow a\right) \in P \operatorname{gdw} \delta\left(q_1, a\right) \in F$, und
- $\left(q_0 \rightarrow \epsilon\right) \in P$ gdw $q_0 \in F$,
ist von [[Chomsky-Hierarchie|Typ 3]] und erfüllt $L(M)=L(G)$.

