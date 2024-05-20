Grundlagen der syntaktischen Analyse von Programmiersprachen, Parsing, Compilerbau.

# Fakten
Kontextfreie Grammatiken dienen zur Spezifikation von Sprachen. 

# Arithmetische Ausdrücke
$$\begin{array}{l}
<\text { Expr> } \rightarrow \text { <Term }>\\
\text { <Expr> } \rightarrow \text { <Expr> }+<\text { Term }>\\
<\text { Term }>\rightarrow<\text { Factor }>\\
<\text { Term }>\rightarrow<\text { Term }>*<\text { Factor }>\\
<\text { Factor }>\rightarrow a\\
<\text { Factor }>\rightarrow(<\text { Expr }>)
\end{array}$$

# Syntaxbaum
Zum validieren von Wörtern 
[[Syntaxbaum]]



# Formale Definition
Eine kontextfreie Grammatik $G=(V, \Sigma, P, S)$ ist ein 4-Tupel:
$V$ ist eine endliche Menge von Nichtterminalzeichen (oder Variablen),
$\Sigma$ ist ein Alphabet von Terminalzeichen, disjunkt von $V$,
$P \subseteq V \times(V \cup \Sigma)^*$ ist eine endliche Menge von Produktionen und $S \in V$ ist das Startsymbol.

Konventionen:
- $A, B, C, \ldots$ sind Nichtterminale,
- $a, b, c, \ldots$ (und Sonderzeichen wie $+, *, \ldots$ ) sind Terminale,
- $\alpha, \beta, \gamma, \ldots \in(V \cup \Sigma)^*$
- Produktionen schreiben wir $A \rightarrow \alpha$ statt $(A, \alpha) \in P$.
- Statt $A \rightarrow \alpha_1, A \rightarrow \alpha_2, A \rightarrow \alpha_3$ schreiben wir einfach $A \rightarrow \alpha_1\left|\alpha_2\right| \alpha_3$
____
#### Weitere Definition
Eine kontextfreie Grammatik $G=(V, \Sigma, P, S)$ erzeugt die Sprache
$L(G):=\left\{w \in \Sigma^* \mid S \rightarrow_G^* w\right\}$

Eine Sprache $L \subseteq \Sigma^*$ heißt kontextfrei gdw es eine kontextfreie Grammatik $G$ gibt mit $L=L(G)$.

Abkürzungen:
- CFG Kontextfreie Grammatik (context-free grammar)
- CFL Kontextfreie Sprache (context-free language)

Konvention:
Ist $G$ aus dem Kontext eindeutig ersichtlich, so schreibt man auch nur $\alpha \rightarrow \beta$ statt $\alpha \rightarrow_G \beta$.





# Beispiele

### Beispiel 1
Die nicht-reguläre Sprache $L=\left\{a^n b^n \mid n \in \mathbb{N}\right\}$ ist kontextfrei, da sie von der CFG
$S \rightarrow a S b \mid \epsilon$
erzeugt wird. Genauer: $L=L(G)$ wobei $G=(V, \Sigma, P, S)$ mit
$$\begin{equation*}
\begin{aligned}
V & =\{S\} \\
\Sigma & =\{a, b\} \\
P & =\{S \rightarrow a S b \mid \epsilon\}
\end{aligned}
\end{equation*}$$

Der unendliche Baum aller möglichen (Links-)Ableitungen:
$$\begin{equation*}
\begin{array}{rllllllll}
S & \rightarrow & a S b & \rightarrow & a^2 S b^2 & \rightarrow & a^3 S b^3 & \rightarrow & \ldots \\
& \searrow & \searrow & & \searrow & & \searrow & \\
& \epsilon & & a b & & a^2 b^2 & & & a^3 b^3
\end{array}
\end{equation*}$$



### Beispiel 2: Palindrome
Die nicht-reguläre Sprache der Palindrome $\left(w=w^R\right)$ über $\{a, b\}$ wird von folgender CFG erzeugt:
$S \rightarrow \epsilon|a| b|a S a| b S b$

Der Anfang des unendlichen Baums aller ([[Linksableitung|Links]]-)Ableitungen (Achtung, dies ist kein Syntaxbaum!):
![[Screenshot 2024-05-16 at 14.41.55.png]]