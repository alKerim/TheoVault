$[a]_{\approx}:=\{b \mid a \approx b\}$

Es gilt:
$[a]_{\approx}=[b]_{\approx} \Leftrightarrow a \approx b$



# Allgemeine Erklärung
Basically "Menge der Präfix-Wörter, die die gleiche Residualsprache haben"

Beispielaufgabe: $L(a^*b^*c^*)$
finde das alphabetisch kleinste Wort für die Äquivalenzklasse, die das Wort $ab$ enthält.
-> Die Äquivalenzklasse von $a b$ ist die Menge von Wörtern, die die gleiche Residualsprache haben wie $a b$. Wenn man sich das mit dem minimalen Automaten vorstellt, sind es die Wörter, die von $q_0$ aus in den gleichen Zustand führen wie das Wort $a b$.
Die Residualsprache $L^{a b}$ ist dagegen die Menge der Wörter, die von diesem Zustand aus in einen (beliebigen) Endzustand führen (wie du richtig gesagt hast: $b^* c^*$ ).
Deshalb: $[ab]_{\equiv_L}=[b]_{\equiv_L}=\{ ab,b,bb,bbbb,aaaabbbbb, ... \}$
	weil nach Angabe $\{ab\}L^{ab}=L$ und wir haben herausgefunden $\{ab,b,...\}L^{ab}=L$
[Source: Zulip](https://zulip.in.tum.de/#narrow/stream/2184-THEO-SS24-Blatt-04/topic/.C3.9C4.2E2.20Automata.20Tutor)

#### Definition von Äquivalenklasse anhand Residualsprache
Für jedes Wort $w$ kannst du die Residualsprache $L^w$ berechnen und die Äquivalenzklasse von $a b$ ist dann $\{w \in \Sigma^* \mid L^w=L^{a b}\}$

#### Strategie um Äquivalenzklassen zu finden
Du kannst dir ja mal einen Automaten für die Sprache aufzeichnen, minimieren und dann schauen, in welche Zustände du mit $a b$ und $b$ kommst. Oder überlegen, welche Suffixe nach $a b$ und welche nach $b$ ein Wort in $L\left(a^* b^* c^*\right)$ ergeben.

