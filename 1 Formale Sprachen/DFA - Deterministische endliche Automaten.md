==D==eterministic ==F==inite ==A==utomaton
![[Screenshot 2024-04-26 at 18.24.24.png]]
Eingabewort $b a b a \rightsquigarrow$ Zustandsfolge 0,0,1,2,2.
Erkannte Sprache: Menge der Wörter, die vom Startzustand in einen Endzustand führen.

[[Recognizer]], der nur einmal das Wort durchläuft und in linearer Zeit es akzeptiert oder ablehnt.

# Formale Definition
### Definition
Ein deterministischer endlicher Automat (deterministic finite automaton, DFA) $M=\left(Q, \Sigma, \delta, q_0, F\right)$ besteht aus
- einer endlichen Menge von Zuständen $Q$,
- einem (endlichen) Eingabealphabet $\Sigma$,
- einer (totalen!) Übergangsfunktion $\delta: Q \times \Sigma \rightarrow Q$,
- einem Startzustand $q_0 \in Q$, und
- einer Menge $F \subseteq Q$ von Endzuständen (akzeptierenden Zust.)

### Akzeptierte Sprache
Die von $M$ akzeptierte Sprache ist $L(M)$ :
$$L(M):=\left\{w \in \Sigma^* \mid \hat{\delta}\left(q_0, w\right) \in F\right\},$$

wobei $\hat{\bar{\delta}}: Q \times \Sigma^* \rightarrow Q$ induktiv definiert ist durch ^fbed54
$$\begin{equation*}
\begin{aligned}
\hat{\delta}(q, \epsilon) & =q \\
\hat{\delta}(q, a w) & =\hat{\delta}(\delta(q, a), w) \quad \text { für } a \in \Sigma, w \in \Sigma^* .
\end{aligned}
\end{equation*}$$
( $\hat{\delta}(q, w)$ bezeichnet **den Zustand**, den man aus $q$ mit $w$ erreicht. ) ^cefbf7

Eine Sprache ist [[regulär]] gdw sie von einem DFA akzeptiert wird.
Eigenschaften von $\hat{\delta}$ : 
- $\hat{\delta}(q, a)=\delta(q, a)$.
- $\hat{\delta}(q, w a)=\delta(\hat{\delta}(q, w), a)$.


# Graphische Darstellung
- Endliche Automaten können durch gerichtete und markierte **Zustandsgraphen** veranschaulicht werden:
	- Knoten $\widehat{=}$ Zuständen
	- Kanten $\widehat{=}$ Übergängen: $p \xrightarrow{a} q \widehat{=} \delta(p, a)=q$
- Der Anfangszustand wird durch einen Pfeil, Endzustände werden durch doppelte Kreise gekennzeichnet.


# Beispiele
![[Screenshot 2024-04-26 at 19.11.48.png]]
![[Screenshot 2024-04-26 at 19.19.16.png|550]]
![[Screenshot 2024-04-28 at 15.53.21.png]]
