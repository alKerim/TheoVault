a.k.a. PDA (pushdown automaton)
![[Screenshot 2024-06-03 at 14.55.04.png|350]]
# Leerer Stack vs. Finalzustände
$L_\epsilon(A)$ oder $L_F(A)$


# Variationen
[[DPDA]]

# Formale Definition
Ein (nichtdeterministischer) Kellerautomat $M=\left(Q, \Sigma, \Gamma, q_0, Z_0, \delta, F\right)$ besteht aus
- einer endlichen Menge von Zuständen $Q$,
- einem endlichen Eingabealphabet $\Sigma$,
- einem endlichen Kelleralphabet $\Gamma$,
- einem Anfangszustand $q_0$,
- einem untersten Kellerzeichen $Z_0$,
- einer Übergangsfunktion $\delta: Q \times(\Sigma \cup\{\epsilon\}) \times \Gamma \rightarrow \mathcal{P}_e\left(Q \times \Gamma^*\right)$, (Hierbei bedeutet $\mathcal{P}_e$ die Menge aller endlichen Teilmengen)
	$\delta(q, \alpha, Z) = \{ (q^{'},XY),(q^{''},\epsilon) \}$  wobei $X,Y \in \Gamma$ 
- einer Menge $F \subseteq Q$ von Endzuständen.

Intuitive Bedeutung von $\left(q^{\prime}, \alpha \right) \in \delta(q, \alpha, Z)$ :
Wenn sich $M$ in Zustand $q$ befindet, das Eingabezeichen a liest, und $Z$ das oberste Kellerzeichen ist, so kann $M$ im nächsten Schritt in $q^{\prime}$ übergehen und $Z$ durch $\alpha$ ersetzen. ^b4c8c3

# Konfiguration der Transitionen
#theo/wichtig 
Eine Konfiguration eines Kellerautomaten $M$ ist ein Tripel $(q, w, \alpha)$ mit $q \in Q, w \in \Sigma^*$ und $\alpha \in \Gamma^*$.
Die Anfangskonfiguration von $M$ für die Eingabe $w \in \Sigma^*$ ist $\left(q_0, w, Z_0\right)$.

Intuitiv stellt eine Konfiguration $(q, w, \alpha)$ eine "Momentaufnahme" des Kellerautomaten dar:
- Der momentane Zustand ist $q$.
- Der noch zu lesende Teil der Eingabe ist $w$.
- Der aktuelle Kellerinhalt ist $\alpha$ (das oberste Kellerzeichen ganz links stehend).
#### Binäre Relation
Auf der Menge aller Konfigurationen definieren wir eine binäre Relation $\rightarrow_M$ wie folgt:
$$\begin{equation*}
(q, a w, Z \alpha) \rightarrow_M\left\{\begin{array}{ll}
\left(q^{\prime}, w, \beta \alpha\right) & \text { falls }\left(q^{\prime}, \beta\right) \in \delta(q, a, Z) \\
\left(q^{\prime}, a w, \beta \alpha\right) & \text { falls }\left(q^{\prime}, \beta\right) \in \delta(q, \epsilon, Z)
\end{array}\right.
\end{equation*}$$

Die [[Reflexiv transitive Hülle|reflexive und transitive Hülle]] von $\rightarrow_M$ wird mit $\rightarrow_M^*$ bezeichnet.
Intuitive Bedeutung von $(q, w, \alpha) \rightarrow_M\left(q^{\prime}, w^{\prime}, \alpha^{\prime}\right)$ :
Wenn $M$ sich in der Konfiguration $(q, w, \alpha$ ) befindet, dann kann er in einen Schritt in die Nachfolgerkonfiguration $\left(q^{\prime}, w^{\prime}, \alpha^{\prime}\right)$ übergehen.

Achtung: eine Konfiguration kann mehrere Nachfolger haben ([[Nichtdeterminismus]]!)

#### Erweiterungslemma
nicht relevant für uns (hat er in VL gesagt)
$$\begin{equation*}
(q, u, \alpha) \rightarrow_M^n\left(q^{\prime}, u^{\prime}, \alpha^{\prime}\right) \Longrightarrow(q, u v, \alpha \beta) \rightarrow_M^n\left(q^{\prime}, u^{\prime} v, \alpha^{\prime} \beta\right)
\end{equation*}$$
# Regeln/Sätze
#theo/wichtig #theo/beweis 
$L(G)=L_\epsilon(M)$ 
(Beweisen, dass eine Grammatik, gleich einem PDA leerer Stack ist, [[Beweisen#$L(G) subseteq L $|wie hier]])
Beweis:
$$\begin{equation*}
\begin{array}{l}
u \in L(G) \\
\Leftrightarrow S \rightarrow_G^* u \text { mit Linksableitung } \\
\Leftrightarrow(q, u, S) \rightarrow_M^*(q, \epsilon, \epsilon) \\
\Leftrightarrow u \in L_\epsilon(M)
\end{array}
\end{equation*}$$


# Spezialfälle
- **POP**-Operation: $\alpha=\epsilon$.
	Das oberste Kellerzeichen $Z$ wird entfernt.

- **PUSH**-Operation: $\alpha=Z^{\prime} Z$.
	$Z^{\prime}$ wird als neues oberstes Kellerzeichen ge**PUSH**t.

- $\epsilon$-Übergang $\quad a=\epsilon$.
	Ohne Lesen eines Eingabezeichens.

Aufgabe: Jeder Schritt kann durch eine Sequenz von diesen drei Operationen simuliert werden. (Hilfszustände verwenden.)



# PDA akzeptiert Wörter
#### Zwei Arten der Akzeptanz
- Akzeptanz durch Endzustände $L_F(M)$ und 
- leeren Keller $L_\epsilon\left(M\right)$

Die beiden sind gleich mächtig.

#### PDA $M$ akzeptiert $w \in \Sigma^*$
- Ein PDA $M$ akzeptiert $w \in \Sigma^*$ mit Endzustand gdw
	$\left(q_0, w, Z_0\right) \rightarrow_M^*(f, \epsilon, \gamma)$ für ein $f \in F, \gamma \in \Gamma^*$.
$$\begin{equation*}
L_F(M):=\left\{w \mid \exists f \in F, \gamma \in \Gamma^* .\left(q_0, w, Z_0\right) \rightarrow_M^*(f, \epsilon, \gamma)\right\}
\end{equation*}$$
- Ein PDA $M$ akzeptiert $w \in \Sigma^*$ mit leeren Keller gdw
	$\left(q_0, w, Z_0\right) \rightarrow_M^*(q, \epsilon, \epsilon)$ für ein $q \in Q$.
$$\begin{equation*}
L_\epsilon(M):=\left\{w \mid \exists q \in Q .\left(q_0, w, Z_0\right) \rightarrow_M^*(q, \epsilon, \epsilon)\right\}
\end{equation*}$$

Konvention: Wir blenden die $F$-Komponente von $M$ aus, wenn wir nur an $L_\epsilon(M)$ interessiert sind.




# Konvertierung: Endzustand -> leerer Keller
#theo/zeit 
$Z u$ jedem PDA $M=\left(Q, \Sigma, \Gamma, q_0, Z_0, \delta, F\right)$ kann man in **linearer Zeit** einen PDA $M^{\prime}=\left(Q^{\prime}, \Sigma, \Gamma^{\prime}, q_0^{\prime}, Z_0^{\prime}, \delta^{\prime}\right)$ konstruieren mit $L_F(M)=L_\epsilon\left(M^{\prime}\right)$.
#theo/wichtig bei PDA mit leerem stack lassen wir einfach das F weg in der formalen Schreibweise.

Ziel:
$$\begin{equation*}
\left(q_0, w, Z_0\right) \rightarrow_M^*(f, \epsilon, \gamma) \Leftrightarrow\left(q_0^{\prime}, w, Z_0^{\prime}\right) \rightarrow_{M^{\prime}}^*(q, \epsilon, \epsilon)
\end{equation*}$$
![[Screenshot 2024-06-06 at 14.45.18.png]]

# Konvertierung: leerer Keller -> Endzustand
**Einfach**: die Transitionen die den Keller leeren würden, in einen Endzustand leiten.



# Konvertierung von/zu [[Kontextfreie Grammatiken|CFGs]]
[[CFG -> PDA]]

