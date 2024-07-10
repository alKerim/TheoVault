#theo/cheatsheet 

## Beweise
### $A A^*=A^* \Longrightarrow \varepsilon \in A$
HA1
Wahr. Sei $A^*=A A^*$. Da $\varepsilon \in A^*$ gilt, folgt auch $\varepsilon \in A A^*$. Deshalb folgt $\varepsilon=u v$ mit $u \in A, v \in A^*$. Dann muss $u=\varepsilon$ sein und daher auch $\varepsilon \in A$.

_____
### $A(B C)=(A B) C$
Wahr. Nutze die Assoziativität von Konkatenation auf Wörtern:
$$\begin{equation*}
\begin{aligned}
u \in A(B C) & \Longleftrightarrow u=v(x y) \text { für } v \in A, x \in B, y \in C \\
& \Longleftrightarrow u=(v x) y \text { für } v \in A, x \in B, y \in C \\
& \Longleftrightarrow u \in(A B) C
\end{aligned}
\end{equation*}$$
____

## Gegenbeispiele
### $A B \backslash A C=A(B \backslash C)$
Falsch. $A:=\{a, a a\}, B:=\{a b\}, C:=\{b\}$, also gelten $A B \backslash A C=\{a a a b\}$ und $A(B \backslash C)=\{a a b, a a a b\}$.
____
### $|A B| \geq|A|$
Falsch. $A:=\{a\}, B:=\emptyset$
____
### $A \subseteq B \Leftrightarrow A^{+} \subseteq B^{+}$
Falsch. $A:=\{a a\}, B:=\{a\}$, womit $A^{+} \subseteq B^{+}$gilt, $A \subseteq B$ aber nicht.
____
### $|A \times A|=|A A|$
==EASY==
Falsch. Sei $A:=\{\varepsilon, a\}$. Dann ist $|A \times A|=|\{(\varepsilon, \varepsilon),(\varepsilon, a),(a, \varepsilon),(a, a)\}|=4$ aber $|A A|=|\{\varepsilon, a, a a\}|=3$

