# Erklärung anhand Beispiel
**AT-Aufgabe H2.2. (Produktmengenkonstruktion) (SS22)**
Konvertieren sie folgenden [[NFA - Nichtdeterministische endliche Automaten|NFA]] über dem Alphabet $\Sigma=\{a, b\}$ zu einem [[DFA - Deterministische endliche Automaten|DFA]], z.B. indem Sie die ***Potenzmengenkonstruktion*** aus der Vorlesung verwenden.
![[Potenzmengenkonstruktion-Aufgabenstellung.png|400]]
Lösung:
![[Potenzmengenkonstruktion-Beispiel.jpeg]]

+sehr wichtig: überall wo es leer bleibt ????
1 Endzustand in einem Merged-Zustand ist genug damit es ein Endzustand ist.

# Formale Definition:
### Beweis
Sei $N=\left(Q, \Sigma, \delta, q_0, F\right)$ ein NFA.
Definiere den DFA $M=\left(\mathcal{P}(Q), \Sigma, \bar{\delta},\left\{q_0\right\}, F_M\right)$ :
$$
F_M:=\{S \subseteq Q \mid S \cap F \neq \emptyset\}
$$
Dann gilt:
$$
\begin{array}
ww \in L(N) & \Leftrightarrow \hat{\bar{\delta}}\left(\left\{q_0\right\}, w\right) \cap F \neq \emptyset & \text { Def. }
\end{array}
$$
[[NFA - Nichtdeterministische endliche Automaten#^c07332|here is the Rule for the line above]]
$$
	\begin{array}{rlrl}
	& \Leftrightarrow \hat{\bar{\delta}}\left(\left\{q_0\right\}, w\right) \in F_M & & \text { Def. } \\
	& \Leftrightarrow w \in L(M) & & \text { Def. }
	\end{array}
	$$
Dies nennt man die Potenzmengen- oder Teilmengenkonstruktion.
In der Praxis werden nur die aus $q_0$ erreichbaren Zuständen konstruiert.

Trotzdem: Für einen NFA mit $n$ Zuständen kann der entsprechende DFA bis zu $2^n$ Zustände haben.

