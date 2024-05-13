- Reguläre Ausdrücke sind eine alternative Notation für die Definition von formalen Sprachen.
- Werden oft in Kombination mit [[Grammatik|Grammatiken]] verwendet.
- Eine Sprache $L \subseteq \Sigma^*$ ist genau dann durch einen regulären Ausdruck darstellbar, wenn sie [[regulär]] ist.


# Definition
Reguläre Ausdrücke (regular expressions, REs) sind induktiv definiert:
- $\emptyset$ ist ein regulärer Ausdruck.
- $\epsilon$ ist ein regulärer Ausdruck.
- Für jedes $a \in \Sigma$ ist $a$ ist ein regulärer Ausdruck.
- Wenn $\alpha$ und $\beta$ reguläre Ausdrücke sind, dann auch
	- $\alpha \beta$
	- $\alpha \mid \beta \quad$ (oft $\alpha+\beta$ geschrieben)
	- $\alpha^*$
- Nichts sonst ist ein regulärer Ausdruck.

$*$ ist die Kleene'sche Iteration (Kleene iteration, Kleene star).

Bindungsstärke: * bindet stärker als Konkatenation stärker als |
- $a b^*=a\left(b^*\right) \neq(a b)^*$
- $a b|c=(a b)| c \neq a(b \mid c)$



# Rekursive Definition der Sprache
Zu einem regulären Ausdruck $\gamma$ ist die zugehörige Sprache $L(\gamma)$ rekursiv definiert:
- $L(\emptyset)=\emptyset$, 
- $|L(\emptyset)|=0$
- $|L(\epsilon)|=1$
- $L(\boldsymbol{\epsilon})=\{\epsilon\}$
- $L(a)=\{a\}$
- $L(\alpha \beta)=L(\alpha) L(\beta)$
- $L(\alpha \mid \beta)=L(\alpha) \cup L(\beta)$
- $L\left(\alpha^*\right)=L(\alpha)^*$


# Regeln
- $\emptyset|\alpha \equiv \alpha| \emptyset \equiv \alpha$
- $\emptyset \alpha \equiv \alpha \emptyset \equiv \emptyset$
- $\boldsymbol{\epsilon} \alpha \equiv \alpha \epsilon \equiv \alpha$
- $\emptyset^* \equiv \epsilon$
- $\epsilon^* \equiv \epsilon$
- $\epsilon \emptyset = \emptyset \epsilon =\emptyset$
- $A \cup \emptyset=\{x \mid x \in A\}=A$
Assoziativität:
- $(\alpha \mid \beta)|\gamma \equiv \alpha|(\beta \mid \gamma)$
- $(\alpha \beta) \gamma \equiv \alpha(\beta \gamma)$
Kommutativität:
- $\alpha|\beta \equiv \beta| \alpha$
Distributivität:
- $\alpha(\beta \mid \gamma) \equiv \alpha \beta \mid \alpha \gamma$
- $(\alpha \mid \beta) \gamma \equiv \alpha \gamma \mid \beta \gamma$
Idempotenz:
- $\alpha \mid \alpha \equiv \alpha$



# Beispiele
### Beispiel 1
Sei das zugrunde liegende Alphabet $\Sigma=\{0,1\}$.
- Alle Wörter, die mit 00 enden:
$$\begin{equation*}
(0 \mid 1)^* 00
\end{equation*}$$
- Alle Wörter gerader Länge, in denen 0 und 1 alternieren:
$$\begin{equation*}
(01)^* \mid(10)^*
\end{equation*}$$
- Alle Wörter, die eine gerade Anzahl von 1 'en enthalten:
$$\begin{equation*}
\left(0^* 10^* 1\right)^* 0^*
\end{equation*}$$
- Alle Wörter, die die Binärdarstellung einer durch 3 teilbaren Zahl darstellen, also
$$\begin{equation*}
0,11,110,1001,1100,1111,10010, \ldots
\end{equation*}$$


### Beispiel 2
Gleitkommazahlen: $\Sigma=\{.,-, 0,1,2,3,4,5,6,7,8,9\}$
$$\begin{equation*}
(-\mid \epsilon)\left(D D^*\left|D D^* . D^*\right| D^* . D D^*\right)
\end{equation*}$$
wobei $D=(0|1| 2|3| 4|5| 6|7| 8 \mid 9)$
Version von Beispiel 3.6:
$$\begin{equation*}
0 \mid(-\mid \epsilon)\left(E D^* \mid\left(0 \mid E D^*\right) . D^* E\right)
\end{equation*}$$
wobei $D=(0|1| 2|3| 4|5| 6|7| 8 \mid 9)$ und $E=(1|2| 3|4| 5|6| 7|8| 9)$


