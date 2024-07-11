
- [ ] Basics
	- [ ] [[Basics Sheet]]
	- [ ] [[regulär]] gdw's

- [ ] Sprachen Regeln
	- [ ] Operationen auf Sprachen
		- [ ] EDGE CASES von CheatSheet refactoren
		- [ ] [[Sprache#Operationen auf Sprachen]]
	- [ ] RE Regeln
	- [ ] Liste kleiner Beweise
		- [ ] $A^*=A^{+} \text {genau dann wenn (gdw.) } \varepsilon \in A$  |   (Ü1.7 a) )
			Die Aussage ist wahr. Wir zeigen beide Richtungen der Aussage getrennt.
			$\Longleftarrow$ : Annahme $\varepsilon \in A$. Dann gilt $A=\{\varepsilon\} \cup A=A^0 \cup A$. Per Definition gilt
			$$\begin{equation*}
			A^{+}=\bigcup_{n \geq 1} A^n=A \cup \bigcup_{n \geq 2} A^n=A^0 \cup A \cup \bigcup_{n \geq 2} A^n=\bigcup_{n \geq 0} A^n=A^* \text {. }
			\end{equation*}$$
			$\Longrightarrow$ : Annahme $A^*=A^{+}$. Da $\varepsilon \in A^*$, muss auch $\varepsilon \in A^{+}$gelten. Nach Vorlesung gilt $A^{+}=A A^*$, also folgt $\varepsilon \in A A^*$. Also gibt es $u \in A$ und $v \in A^*$ mit $\varepsilon=u v$. Daraus folgt $u=\varepsilon$ und $v=\varepsilon$. Da $u \in A$ gilt, ist $\varepsilon \in A$ gezeigt.
	- [ ] Zwei Sprachen sind nicht gleich beweisen -> mindestens ein Wort in A das nicht in B ist


- [ ] Grammatiken
	- [ ] ww
	$D:=\left\{w w: w \in\{a, b\}^*\right\} \quad$ (schwierig)
	$G:=(\{S, X, O, A, B\},\{a, b\}, P, S)$ mit Produktionen $P$ wie folgt
	$$\begin{equation*}
	\begin{array}{lll}
	S \rightarrow X O & O \rightarrow \varepsilon & X \rightarrow X a A|X b B| \varepsilon \\
	A a \rightarrow a A & B a \rightarrow a B & A O \rightarrow O a \\
	A b \rightarrow b A & B b \rightarrow b B & B O \rightarrow O b
	\end{array}
	\end{equation*}$$
	Wir schreiben alle Buchstaben das Wortes doppelt und verschieben $A$ und $B$ bis zum Ende (markiert mit $O$ ) und wandeln dort das Zeichen wieder um.
- [ ] Konstruieren: 
	- [ ] [[Grammatiken konstruieren]]
	- [ ] PDAs
	- [ ] TM konstruieren




______
# Strukturelle Induktion
![[Strukturelle Induktion#Algorithmus (Induktionsbeweis) - Beispiel]]

![[Strukturelle Induktion#Important Rules]]



# Algorithmen

## Konvertierungen 
### Automaten (NFA, DFA)
#### $\epsilon$-NFA -> NFA
[[ε-NFA -> NFA]]

#### RE <-> $\epsilon$-NFA
[[RE -> ε-NFA]]
[[ε-NFA -> RE]]

#### NFA -> RE (lösung durch gleichungssystem - Ardens Lemma)
[[NFA -> RE (Ardens Lemma)]]


#### NFA -> DFA (Potenzmengen-Konstruktion)
[[NFA -> DFA (Potenzmengenkonstruktion)]]


#### Rechtslineare Grammatik -> NFA
[[Rechtslineare Grammatik zu NFA (und zurück)#Rechtslineare Grammatik -> NFA]]

#### NFA -> Rechtslineare Grammatik
[[Rechtslineare Grammatik zu NFA (und zurück)#NFA -> Rechtslineare Grammatik]]


_____
#### Merging
##### DFA + DFA
[[DFA + DFA (Produkt-konstruktion)]]

##### NFA + NFA 
1. [[NFA -> DFA (Potenzmengenkonstruktion)]]
2. [[DFA + DFA (Produkt-konstruktion)]]

_____
#### Minimierung
[[Minimierungsalgorithmus]]
TODO: Eine beispielsaufgabe

____
#### CFG -> CNF
[[CNF-Algorithmus]]

### Automaten (PDA)
##### CFG -> PDA
[[CFG -> PDA]]

##### PDA -> CFG
[[PDA -> CFG]]

## CYK (Wortproblem)
[[CYK Algorithmus]]
## Nützliche Nichtterminale
[[nützlich, erzeugend, erreichbar]]
[[nützlich, erzeugend, erreichbar#Elimination Algorithmus|Eliminations-Algorithmus für nicht-nützliche Terminale]]

# Pumping Lemma
TODO: GET FROM ADRIAN FOLIEN
### PL reguläre Sprachen
- nicht-regulär: [[Pumping Lemma#Pumping Lemma für reguläre Sprachen]] adrian folien
- PL gilt: adrian folien

### PL kontextfreie Sprachen
- nicht kontextfrei: [[Pumping Lemma für kontextfreie Sprachen#Template Beispielaufgabe (Endterm23)]]
- PL gilt: adrian folien



# Residualsprachen
### Unterschied beweisen


### Unendliche Residualsprachen beweisen
siehe auch [[paarweise verschiedene Residualsprachen]]
Beispielaufgabe: [H5.4 b) (unendlich Residualsprachen)](https://teaching.model.in.tum.de/2024ss/theo/ex/ha05-solution.pdf?key=IlGKpVDe)
Theo-S05.pdf (Adrian Folien)
![[Screenshot 2024-07-05 at 15.40.42.png]]


