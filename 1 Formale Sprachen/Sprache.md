Eine Teilmenge $L \subseteq \Sigma^{*}$ ist eine (formale) Sprache.
$\Sigma^{*}$ ist die [[Menge aller Wörter]].


____
#theo/basics/sprachen
Jede Sprache ist [[abzählbar]], aber nicht jede Sprache ist [[rekursiv aufzählbar]] (s.u.)
____

# Beispielsprachen
- Die Menge aller Wörter im Duden
- Die Menge der deutschen Sätze ist ==keine **formale** Sprache !!==
$$\begin{equation*}
\begin{array}{l}
L_1=\{\epsilon, a b, a b a b, a b a b a b, \ldots\}=\left\{(a b)^n \mid n \in \mathbb{N}\right\} \\
\left(\Sigma_1=\{a, b\}\right) \\
L_2=\{\epsilon, a b, a a b b, a a a b b b, \ldots\}=\left\{a^n b^n \mid n \in \mathbb{N}\right\} \\
\left(\Sigma_2=\{a, b\}\right) \\
L_3=\{\epsilon, 1,100,1001,10000, \ldots\}= \\
\left\{w \in\{0,1\}^* \mid w \text { ist eine binär kodierte Quadratzahl }\right\} \\
\left(\Sigma_3=\{0,1\}\right) \\
\emptyset \\
\{\epsilon\}
\end{array}
\end{equation*}$$
- $\epsilon$ oder $ab$ sind ==keine Sprachen !!==



# Operationen auf Sprachen
### Konkatenation von Sprachen
Seien $A, B \subseteq \Sigma^*$
- Konkatenation: $A B=\{u v \mid u \in A \wedge v \in B\}$
	Bsp: $\{a b, b\}\{a, b b\}=\{a b a, a b b b, b a, b b b\}$
	NB: $\{a b, b\} \times\{a, b b\}=\{(a b, a),(a b, b b),(b, a),(b, b b)\}$
- $A^{n}=\left\{w_1 \ldots w_n \mid w_1, \ldots, w_n \in A\right\}=\underbrace{A \cdots A}_{n}$
	Bsp: $\{a b, b a\}^2=\{a b a b, a b b a, b a a b, b a b a\}$
	Rekursiv: $A^0=\{\epsilon\}$ und $A^{n+1}=A A^n$
- $A^{*}=\left\{w_1 \ldots w_n \mid n \geq 0 \wedge w_1, \ldots, w_n \in A\right\}=\bigcup_{n \in \mathbb{N}} A^n$
	Bsp: $\{01\}^*=\{\epsilon, 01,0101,010101, \ldots\} \neq\{0,1\}^*$
	Leere Wort ist immer enthalten in $A^*$
	weil $\epsilon \in A^0$, und das gilt IMMER. Deshalb auch $\epsilon \in \Sigma^0$ 
- $A^{+}=A A^*=\bigcup_{n \geq 1} A^n$

Bsp: $\Sigma^{+}=$Menge aller nicht-leeren Wörter über $\Sigma$

### Rechenregeln für Sprachen
- $\emptyset A=\emptyset$ #theo/basics
- $\emptyset | \alpha = \alpha$ 
- $\{\epsilon\} A=A$ #theo/basics
- Für alle $A: \epsilon \in A^*$
- $\emptyset^*=\{\epsilon\}$ #theo/basics 
- $A \times \emptyset = \emptyset$ 
- $\emptyset \in L$ für wirklich jede einzelne Sprache $L \subseteq \Sigma^*$ #theo/basics

Abschlusseigenschaften
- $A(B \cup C)=A B \cup A C$
- $(A \cup B) C=A C \cup B C$
- **Achtung**: i.A. gilt $A(B \cap C)=A B \cap A C$ nicht. ^11dae2
- $A^{*} A^{*}=A^{*}$
- **Tricks**
	- $A \cup \bar{A} = \Sigma^*$ ... dies gilt für jede/egal welche Sprache
		Mindshift: Wenn $A,B$ Sprachen mit $B=\bar{A}$ dann gilt $A \cup B = \Sigma^*$
	- $A \cap \bar{A} = \emptyset$ ... dies gilt für jede/egal welche Sprache




# Endliche / Unendliche Sprache
### Endlich
#theo/basics/sprachen 
Eine Sprache wird als endlich bezeichnet, wenn sie eine endliche Anzahl von Wörtern enthält. Zum Beispiel ist die Sprache $\{a, a a, a a a\}$ endlich, weil sie genau drei Wörter enthält.

**Endliche Sprachen** können immer von einem endlichen Automaten ([[Endliche Automaten]], [[Endliche Automaten und reguläre Ausdrucke]]) akzeptiert werden, da der Automat nur eine endliche Anzahl von Zuständen benötigt, um jedes Wort in der Sprache zu erkennen

##### Beispiel endliche Sprache
$S \rightarrow  b \mid a$

### Unendlich
#theo/basics/sprachen 
Eine Sprache ist unendlich, wenn sie unendlich viele Wörter enthält. Beispielsweise ist die Sprache aller Wörter über dem Alphabet $\{a\}$, also $\{a, a a, a a a, \ldots\}$, unendlich.



Produktion:
- **Unendliche Sprachen** können von verschiedenen Typen von Automaten erkannt werden, abhängig von ihrer Komplexität. Zum Beispiel kann ein einfacher deterministischer endlicher Automat ([[DFA - Deterministische endliche Automaten|DFA]]) oder ein nichtdeterministischer endlicher Automat ([[NFA - Nichtdeterministische endliche Automaten|NFA]]) viele unendliche Sprachen erkennen, aber nicht alle. Manche unendliche Sprachen benötigen leistungsfähigere Rechenmodelle wie Kellerautomaten oder Turingmaschinen, insbesondere wenn sie eine komplexere Struktur haben.
- Unendliche Sprachen benötigen typischerweise rekursive Produktionsregeln in Grammatiken, um eine unendliche Anzahl von Wörtern zu generieren. Diese Sprachen können oft durch [[Kontextfreie Grammatiken|kontextfreie]] oder kontextsensitive Grammatiken beschrieben werden, abhängig von ihrer spezifischen Struktur und den benötigten Regeln.

##### Beispiel unendliche Sprache
$S \rightarrow a S \mid b$

##### Beispiel unendliche Sprache -> endliche Sprache
Nehmen wir $S \rightarrow a S \mid b$. Durch Löschen von $a$ erhalten wir $S \rightarrow S \mid b$. [^1]





# Sprachen Beispiele
[[Sprachen Beispiele]]


[^1]: Q1.6. von [[Quiz 1]]