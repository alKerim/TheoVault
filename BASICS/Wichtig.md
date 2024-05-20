
[[Induktive Definition#^4db48b]]


# $\Sigma^* L=\Sigma^*$ gdw $\epsilon \in L$ 
Zusammengefasst gilt $\Sigma^* L=\Sigma^*$ genau dann, wenn die Sprache $L$ das leere Wort $\epsilon$ enthält. Wenn $L$ das leere Wort nicht enthält, dann ist $\Sigma^* L$ eine echte Teilmenge von $\Sigma^*$.
	Beispielaufgabe:
	Mehrfachauswahl. Welche der folgenden Aussagen gelten für alle regulären Sprachen $L_1 \subseteq\{a, b\}^*$, und nicht regulären Sprachen $L_2 \subseteq\{a, b\}^*$ ?
	✅(a) Wenn $L_1 \neq \emptyset$, dann ist $L_1\{c\} L_2$ nicht regulär
	✅(b) Es gibt keine reguläre Sprache $L$ mit $L_1 \backslash L=L_2$
	❌(c) $L_1 L_2$ ist nicht regulär
		Gegenbeispiel: $L_{1}= \Sigma^*$ und $L_2$ ist nicht regulär und $\epsilon \not \in L_2$
	❌(d) $L_1 L_2$ ist regulär
		Gegenbeispiel: $L_{1}= \Sigma^*$ und $L_2$ ist nicht regulär und $\epsilon \in L_2$ dann $L_{1}L_{2}= \Sigma^*$


_____
# Kontextfreie schwere aufgaben
![[Screenshot 2024-05-20 at 17.17.56.png]]
Rule 1: for every a there has to come a b
Rule 2: for every c there has to come a b
Rule 3: as many b's can be added as you want
