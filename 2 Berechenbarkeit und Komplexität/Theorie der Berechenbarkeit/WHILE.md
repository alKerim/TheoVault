strukturierte Programme mit while-Schleifen

# Syntax
Wir definieren WHILE- und GOTO-Berechenbarkeit und zeigen ihre Äquivalenz mit [[Uni/8th Semester/Theo 8th/2 Berechenbarkeit und Komplexität/Theorie der Berechenbarkeit/Berechenbarkeit|Turing-Berechenbarkeit]].
Syntax von WHILE-Programmen:
$$\begin{equation*}
\begin{aligned}
P \rightarrow & X:=X+C \\
\mid & X:=X-C \\
\mid & P ; P \\
\mid & \text { IF } X=0 \text { DO } P \text { ELSE } Q \text { END } \\
\mid & \text { WHILE } X \neq 0 \text { DO } P \text { END }
\end{aligned}
\end{equation*}$$
wobei $X$ eine der Variablen $x_0, x_1, \ldots$ und $C$ eine der Konstanten $0,1, \ldots$ sein kann.


# Semantik
Semantik von WHILE-Programmen (informell):
$x_i:=x_j+n \quad$ Neuer Wert von $x_i$ ist $x_j+n$.
$x_i:=x_j-n \quad$ Neuer Wert von $x_i$ ist $x_j \doteq n$.
$P_1 ; P_2 \quad$ Führe zuerst $P_1$ und dann $P_2$ aus.

WHILE $x_i \neq 0$ DO $P$ END Führe $P$ bis die Variable $x_i$ (wenn je) den Wert 0 annimmt.


# Beispiele
#### Beispiel 1
$\text { WHILE } x_2 \neq 0 \text { DO } x_1:=x_0+1 \text { END }$

#### Beispiel 2
WHILE $x_1 \neq 0$ DO $x_2:=x_2+1 ; x_1:=x_1-1$ END simuliert
-> Zu Beginn der Ausführung stehen die Eingaben in $x_1, \ldots, x_k$. Alle anderen Variablen sind 0 . Die Ausgabe wird in $x_0$ berechnet.



# Modifizierte Differenz
Die modifizierte Differenz ist $m \dot{-} n:=\left\{\begin{array}{ll} m-n & \text { falls } m \geq n \\ 0 & \text { sonst } \end{array}\right.$



# WHILE-berechenbar
WHILE- und [[GOTO]]-Berechenbarkeit sind äquivalent. ^d63317
#### totale Funktion
Eine [[total|totale Funktion]] $f: \mathbb{N}^k \rightarrow \mathbb{N}$ ist **WHILE-berechenbar** **gdw** es ein WHILE-Programm $P$ gibt, so dass für alle $n_1, \ldots, n_k \in \mathbb{N}$ : $P$, gestartet mit $n_1, \ldots, n_k$ in $x_1, \ldots, x_k$ ( 0 in den anderen Var.) terminiert mit $f\left(n_1, \ldots, n_k\right)$ in $x_0$.

#### partielle Funktion
Eine [[partiell|partielle Funktion]] $f: \mathbb{N}^k \rightarrow \mathbb{N}$ ist **WHILE-berechenbar** **gdw** es ein WHILE-Programm $P$ gibt, so dass für alle $n_1, \ldots, n_k \in \mathbb{N}$ :
$P$, gestartet mit $n_1, \ldots, n_k$ in $x_1, \ldots, x_k$ ( 0 in den anderen Var.)
- terminiert mit $f\left(n_1, \ldots, n_k\right)$ in $x_0$, falls $f\left(n_1, \ldots, n_k\right)$ definiert ist,
- terminiert nicht, falls $f\left(n_1, \ldots, n_k\right)$ undefiniert ist.

