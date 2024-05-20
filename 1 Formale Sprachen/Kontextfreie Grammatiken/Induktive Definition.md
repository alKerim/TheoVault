Bei [[Kontextfreie Grammatiken]]

# Beispiel: Balancierte Klammern
$$\begin{equation*}
S \rightarrow \epsilon|[S]| S S
\end{equation*}$$

Um zu zeigen, dass diese Grammatik die Menge aller 
balancierten Klammerwörter in $\{[,]\}^*$ erzeugt, 
betrachten wir die Grammatik als induktive Definition einer Sprache $L_G(S)$ :
$$\begin{array}{rlll} 
& & \epsilon \in L_G(S) \\
u \in L_G(S) & \Longrightarrow & {[u] \in L_G(S)} \\
u \in L_G(S) \wedge v \in L_G(S) & \Longrightarrow & u v \in L_G(S)
\end{array}$$
^ Sehr wichtig ^4db48b
Damit gilt zB:
$$\begin{equation*}
\begin{array}{l}
\epsilon \in L_G(S) \Longrightarrow[] \in L_G(S) \Longrightarrow[[]] \in L_G(S) \\
\Longrightarrow[[]][] \in L_G(S)
\end{array}
\end{equation*}$$

# Bemerkungen
- Die Produktionen $(\rightarrow)$ erzeugen Wörter top-down, d.h. von einem Nichtterminal zu einem Wort hin.
- Die induktive Definition $(\Longrightarrow)$ erzeugt Wörter bottom-up, d.h. sie setzt kleinere Wörter zu größeren zusammen.
- Die induktive Definition betrachtet nur Wörter aus $\Sigma^*$.




# Induktionsprinzip

Zur induktiven Definition von $L_G(S)$ gehört ein Induktionsprinzip: Um zu zeigen, dass für alle $u \in L_G(S)$ eine Eigenschaft $P(u)$ gilt, dh $\forall u \in L_G(S) . P(u)$, zeige:
$$\begin{array}{l}
\begin{array}{rlll|} 
& & P(\epsilon) \\
P(u) & \Longrightarrow & P([u]) \\
P(u) \wedge P(v) & \Longrightarrow & P(u v)
\end{array}\\
\text { „Induktion über die Erzeugung von } u^{\prime \prime}
\end{array}$$
Alle $u \in L_G(S)$ enthalten gleich viele $[$ wie $]$.

Beweis:
Mit Induktion über die Erzeugung von $u$ :
- $\epsilon$ enthält $0$ \[ und \].
- Enthält $u$ gleich viele \[ wie \], so auch $[u]$.
- Enthalten $u$ und $v$ gleich viele \[ wie \], so auch $u v$.



# Auswählen von Beweisart
- "w $w \in L_G(S) \Longrightarrow P(w)$ “ beweist man immer schematisch mit Induktion über die Erzeugung von $w$.
	Normalerweise ziemlich mechanisch: das wort von dieser Produktion als letztes erzeugt, dann betrachten wir genau diese Fälle
- "$P(w) \Longrightarrow w \in L_G(S)$ “ beweist man oft mit Induktion über $|w|$. Erfordert meist Kreativität.
	Die Kreativität lag in der Fallunterscheidung. Es gibt eine null in der Mitte, oder es gibt mindestens eine Null in der Mitte



# Beispiele
### Beispiel 1: Gerade Anzahl a's
Grammatik:
$$A \rightarrow \epsilon \mid a B \quad B \rightarrow A a$$Induktive Definition:
- $\epsilon \in L_G(A)$
- $w \in L_G(B) \Longrightarrow a w \in L_G(A)$
- $w \in L_G(A) \Longrightarrow w a \in L_G(B)$

Beim induktiven Beweis von
$\left(w \in L_G(A) \Longrightarrow \#_a(w)\right.$ ist gerade $) \wedge$
$\left(w \in L_G(B) \Longrightarrow \#_a(w)\right.$ ist ungerade)

muss man zeigen
- $\#_a(\epsilon)$ ist gerade
- $\#_a(w)$ ist ungerade $\Longrightarrow \#_a(a w)$ ist gerade
- $\#_a(w)$ ist gerade $\Longrightarrow \#_a(w a)$ ist ungerade





____
Related: [[Induktionsbeweis]]
