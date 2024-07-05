
# Sprachen Regeln
#### Operationen auf Sprachen
EDGE CASES von CheatSheet refactoren
[[Sprache#Operationen auf Sprachen]]

#### RE Regeln

#### Liste kleiner Beweise
##### $A^*=A^{+} \text {genau dann wenn (gdw.) } \varepsilon \in A$  |   (Ü1.7 a) )
Die Aussage ist wahr. Wir zeigen beide Richtungen der Aussage getrennt.
$\Longleftarrow$ : Annahme $\varepsilon \in A$. Dann gilt $A=\{\varepsilon\} \cup A=A^0 \cup A$. Per Definition gilt
\begin{equation*}
A^{+}=\bigcup_{n \geq 1} A^n=A \cup \bigcup_{n \geq 2} A^n=A^0 \cup A \cup \bigcup_{n \geq 2} A^n=\bigcup_{n \geq 0} A^n=A^* \text {. }
\end{equation*}
$\Longrightarrow$ : Annahme $A^*=A^{+}$. Da $\varepsilon \in A^*$, muss auch $\varepsilon \in A^{+}$gelten. Nach Vorlesung gilt $A^{+}=A A^*$, also folgt $\varepsilon \in A A^*$. Also gibt es $u \in A$ und $v \in A^*$ mit $\varepsilon=u v$. Daraus folgt $u=\varepsilon$ und $v=\varepsilon$. Da $u \in A$ gilt, ist $\varepsilon \in A$ gezeigt.




# Grammatiken
#### ww
$D:=\left\{w w: w \in\{a, b\}^*\right\} \quad \text { (schwierig) }$
	$G:=(\{S, X, O, A, B\},\{a, b\}, P, S)$ mit Produktionen $P$ wie folgt
	$$\begin{equation*}
	\begin{array}{lll}
	S \rightarrow X O & O \rightarrow \varepsilon & X \rightarrow X a A|X b B| \varepsilon \\
	A a \rightarrow a A & B a \rightarrow a B & A O \rightarrow O a \\
	A b \rightarrow b A & B b \rightarrow b B & B O \rightarrow O b
	\end{array}
	\end{equation*}$$
	Wir schreiben alle Buchstaben das Wortes doppelt und verschieben $A$ und $B$ bis zum Ende (markiert mit $O$ ) und wandeln dort das Zeichen wieder um.



# Strukturelle Induktion
![[Strukturelle Induktion#Algorithmus (Induktion)]]

![[Strukturelle Induktion#Important Rules]]



# Algorithmen

## Konvertierungen
#### $\epsilon$-NFA -> NFA
[[ε-NFA -> NFA]]

#### RE <-> $\epsilon$-NFA
[[RE -> ε-NFA]]
[[ε-NFA -> RE]]

#### NFA -> RE (lösung durch gleichungssystem - Ardens Lemma)
[[NFA -> RE (Ardens Lemma)]]


#### NFA -> DFA (Potenzmengen-Konstruktion)
[[NFA -> DFA (Potenzmengenkonstruktion)]]
_____
## Merging
#### DFA + DFA
[[DFA + DFA (Produkt-konstruktion)]]

#### NFA + NFA 
1. [[NFA -> DFA (Potenzmengenkonstruktion)]]
2. [[DFA + DFA (Produkt-konstruktion)]]

_____
## Minimierung
TODO: Eine beispielsaufgabe



# Residualsprachen
### Unterschied beweisen


### Unendliche Residualsprachen beweisen
Theo-S05.pdf (Adrian Folien)
![[Screenshot 2024-07-05 at 15.40.42.png]]
