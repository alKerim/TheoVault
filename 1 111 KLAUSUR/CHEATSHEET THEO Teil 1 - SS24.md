
- [x] Basics
	- [x] [[Basics Sheet]] Formale Sprachen
	- [x] Tupel, transitionen von
		- [x] [[NFA - Nichtdeterministische endliche Automaten]]
		- [x] [[Grammatik]]
			- [x] [[Rechtslineare Grammatiken]]
			- [x] [[Kontextfreie Grammatiken]]
			- [x] [[Typ 0]]
		- [x] [[Kellerautomat - PDA]]
	- [x] [[Typ 0]] facts und Auserhalb von Typ 0 definieren
	- [x] [[regulär]] gdw's

- [x] Grammatiken
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
	- [x] $ww^R$ 
	- [x] Menge aller balancierten wörter

- [x] Sprachen Regeln
	- [x] Liste kleiner Beweise
		- [x] $A^*=A^{+} \text {genau dann wenn (gdw.) } \varepsilon \in A$  |   (Ü1.7 a) )
			Die Aussage ist wahr. Wir zeigen beide Richtungen der Aussage getrennt.
			$\Longleftarrow$ : Annahme $\varepsilon \in A$. Dann gilt $A=\{\varepsilon\} \cup A=A^0 \cup A$. Per Definition gilt
			$$\begin{equation*}
			A^{+}=\bigcup_{n \geq 1} A^n=A \cup \bigcup_{n \geq 2} A^n=A^0 \cup A \cup \bigcup_{n \geq 2} A^n=\bigcup_{n \geq 0} A^n=A^* \text {. }
			\end{equation*}$$
			$\Longrightarrow$ : Annahme $A^*=A^{+}$. Da $\varepsilon \in A^*$, muss auch $\varepsilon \in A^{+}$gelten. Nach Vorlesung gilt $A^{+}=A A^*$, also folgt $\varepsilon \in A A^*$. Also gibt es $u \in A$ und $v \in A^*$ mit $\varepsilon=u v$. Daraus folgt $u=\varepsilon$ und $v=\varepsilon$. Da $u \in A$ gilt, ist $\varepsilon \in A$ gezeigt.
	- [x] Zwei Sprachen sind nicht gleich beweisen -> mindestens ein Wort in A das nicht in B ist

- [ ] [[Beweisen]], [[Beweis Types]]
	- [x] $L \subseteq L(G)$, $L(G) \subseteq L$
	- [ ] Beweis Beispiel von Woche 13... [Endterm 2021Aufgabe 9](https://zulip.in.tum.de/user_uploads/2/12/pgg6QBv01c5DzlfTtFhElkOO/Theo-S13_nosolution.pdf#page=10)
Beweis Tipps von Adrian:
	Irgendein Beispiel finden an das man sich
	Struktur finden, die man sich abschauen kann. 
	Beweis Types. 
	Bewei

- [ ] Pumping Lemma
	- [x] regular
		- [x] PL erfüllt: [[Pumping Lemma#Schema wenn wir PL für L beweisen wollen (Also L das PL erfüllt):]]
		- [x] PL nicht regular [[Pumping Lemma#Template für PL reguläre Sprachen]]
	- [ ] kontextfrei
		- [ ] PL erfüllt - NOTHING FOUND
		- [x] PL nicht regulär [[Pumping Lemma für kontextfreie Sprachen#Template Beispielaufgabe (Endterm23)]]


- [x] [[#Strukturelle Induktion]]


- [x] Residualsprachen
	- [x] Definition [[Äquivalenzklasse]]
		- [x] Beispiel
	- [x] zwei residualsprachen unterschiedlich  (Basic)
	- [x] [[#Unendliche Residualsprachen beweisen]]


- [x] Konstruieren: 
	- [x] [[Konstruktion einer Grammatik]]
	- [x] [[Konstruktion eines PDA]]
	- [x] [[Konstruktion einer TM]]

- [ ] Algorithmen
	- [x] [[#Konvertierungen]]
		- [x] e-NFA -> NFA (NO)
		- [x] RE -> e-NFA
		- [x] e-NFA -> RE
		- [x] NFA -> RE (ARDENS LEMMA)
		- [x] NFA -> DFA (Potenzmengen Konstruktion)
		- [x] Rechtsl. Gr. -> NFA
		- [x] NFA -> Rechtsl. Gr.
	- [ ] CFGs
		- [x] CNF Algorithmus
		- [x] CFG -> PDA
		- [x] PDA -> CFG
		- [x] Leerer Stack -> Endzustand
		- [x] Endzustand -> Leerer Stack
	- [ ] DFA + DFA
	- [ ] Minimierung
	- [ ] [[#CYK (Wortproblem)]]
	- [ ] Eliminations-Algorithmus [[#Nützliche Nichtterminale]]


all my daydreams used to be nightmares
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

##### Leerer Stack -> Endzustand
[[Kellerautomat - PDA#Konvertierung leerer Keller -> Endzustand]]

##### Endzustand -> Leerer Stack
[[Kellerautomat - PDA#Konvertierung Endzustand -> leerer Keller]]

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


