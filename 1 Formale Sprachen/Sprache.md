Eine Teilmenge $L \subseteq \Sigma^{*}$ ist eine (formale) Sprache.
$\Sigma^{*}$ ist die [[Menge aller Wörter]].


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
- $A^*=\left\{w_1 \ldots w_n \mid n \geq 0 \wedge w_1, \ldots, w_n \in A\right\}=\bigcup_{n \in \mathbb{N}} A^n$
	Bsp: $\{01\}^*=\{\epsilon, 01,0101,010101, \ldots\} \neq\{0,1\}^*$
	Leere Wort ist immer enthalten in $A^*$
- $A^{+}=A A^*=\bigcup_{n \geq 1} A^n$

Bsp: $\Sigma^{+}=$Menge aller nicht-leeren Wörter über $\Sigma$

**Achtung:**
- Für alle $A: \epsilon \in A^*$
- $\emptyset^*=\{\epsilon\}$


### Rechenregeln für Sprachen
- $\emptyset A=\emptyset$
- $\{\epsilon\} A=A$
- $A(B \cup C)=A B \cup A C$
- $(A \cup B) C=A C \cup B C$
- **Achtung**: i.A. gilt $A(B \cap C)=A B \cap A C$ nicht. ^11dae2
- $A^* A^*=A^*$
