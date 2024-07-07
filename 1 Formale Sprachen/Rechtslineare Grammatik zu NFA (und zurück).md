- Für jede [[Rechtslineare Grammatiken|rechtslineare Grammatik]] $G$ gibt es einen [[DFA - Deterministische endliche Automaten|DFA]] $M$ mit $L(M)=L(G)$.
- Für jeden DFA $M$ gibt es eine rechtslineare Grammatik $G$ mit $L(G)=L(M)$.


# Rechtslineare Grammatik -> NFA
Easy... Einfach jede Produktion in Transitionen Verwandeln
Wichtig: Falls $\epsilon \in$ Grammatik, dann setze $S \in F$ 

via [[theo-folien-handout.pdf#page=41|Satz 3.9]]

$A \rightarrow a$ :
Formal:
$q_f \in \delta(X, a) \operatorname{gdw}(X \rightarrow a) \in P$
Drawing:
TODO
Draw how it would go

$A \rightarrow a B$ :
Formal:
$Y \in \delta(X, a) \operatorname{gdw}(X \rightarrow a Y) \in P$
Draw how it would go ^293a00

$A \rightarrow \epsilon$:
Dann setze $F=\left\{S, q_f\right\}$.

Aufgabe: Und wenn $S \rightarrow a X|a Y| \epsilon$ ?
-> Dann gibt es 2 Endzustände, nämlich jetzt zusatzlich noch der Startzustand

![[Screenshot 2024-07-07 at 11.33.57.png|400]]



### Formaler Beweis
Sei $G=(V, \Sigma, P, S)$ eine rechtslineare Grammatik ohne die Produktion $S \rightarrow \epsilon$. Definiere den NFA $A=\left(Q, \Sigma, \delta, q_0, F\right)$ mit
- $Q=V \cup\left\{q_f\right\}$ (wobei $q_f \notin V$ )
- $Y \in \delta(X, a) \operatorname{gdw}(X \rightarrow a Y) \in P$
- $q_f \in \delta(X, a) \operatorname{gdw}(X \rightarrow a) \in P$
- $q_0=S$
- $F=\left\{q_f\right\}$

Es gilt (Induktion über $n$ ):
$S \rightarrow a_1 X_1 \rightarrow_G a_1 a_2 X_2 \rightarrow_G \cdots \rightarrow_G a_1 \ldots a_{n-1} X_{n-1} \rightarrow_G a_1 \ldots a_n$

ist eine Ableitung von $G$ gdw
$q_f \in \delta\left(S, a_1 \ldots a_n\right) .$

Damit gilt $L(G)=L(A)$. (Fall mit $S \rightarrow \epsilon$ : Aufgabe)




# NFA -> Rechtslineare Grammatik 

Als Gleichungssystem, mit **[[Ardens Lemma]]**
Siehe [[theo-folien-handout.pdf#page=68|hier]]

**[[Ardens Lemma]]** wird benutzt um Gleichungen mit nur einer Variabler zu lösen

Gleichungssysteme lösen: mit Gaußscher 

#### Beweis/Algorithmus
Sei $M=\left(Q, \Sigma, \delta, q_0, F\right)$. 
Die Grammatik $G=(V, T, P, S)$ mit
- $V=Q, T=\Sigma, S=q_0$,
- $\left(q_1 \rightarrow a q_2\right) \in P \operatorname{gdw} \delta\left(q_1, a\right)=q_2$,
- $\left(q_1 \rightarrow a\right) \in P \operatorname{gdw} \delta\left(q_1, a\right) \in F$, und
- $\left(q_0 \rightarrow \epsilon\right) \in P \mathrm{gdw} q_0 \in F$,
ist von Typ 3 und erfüllt $L(M)=L(G)$.


# Beispiele
### Beispiel 1
![[Screenshot 2024-04-28 at 18.18.36.png]]
$$\begin{aligned}
& \hat{\bar{\delta}}(\{p, q\}, 10) \\
= & \hat{\bar{\delta}}(\bar{\delta}(\{p, q\}, 1), 0) \\
= & \hat{\delta}(\delta(p, 1) \cup \delta(q, 1), 0) \\
= & \hat{\bar{\delta}}(\{p, q, r\}, 0) \\
= & \bar{\delta}(\{p, q, r\}, 0) \\
= & \delta(p, 0) \cup \delta(q, 0) \cup \delta(r, 0) \\
= & \{p\} \cup\{r\} \cup \emptyset=\{p, r\}
\end{aligned}$$
### Beispiel 2
Hier sind eine Grammatik und ein NFA, die beide dieselbe Sprache beschreiben
![[Screenshot 2024-04-28 at 18.40.00.png]]