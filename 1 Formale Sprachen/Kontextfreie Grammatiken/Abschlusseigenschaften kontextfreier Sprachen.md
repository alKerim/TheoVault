
# Beispiele für Beweise
#theo/beispiel/beweis 
easy:
#### Beispiel 1: $L_1\cap L_2$
Die Menge der kontextfreien Sprachen ist nicht abgeschlossen unter Durchschnitt oder Komplement.
Beweis:
$L_1:=\left\{a^i b^i c^j \mid i, j \in \mathbb{N}\right\}$ ist kontextfrei
$L_2:=\left\{a^i b^j c^j \mid i, j \in \mathbb{N}\right\}$ ist kontextfrei
$L_1 \cap L_2=\left\{a^i b^i c^i \mid i \in \mathbb{N}\right\}$ ist nicht kontextfrei


# Beweise
OE nehmen wir an, dass $V_1 \cap V_2=\emptyset$.
(1)
$$\begin{equation*}
\begin{array}{l}
V=V_1 \cup V_2 \cup\{S\} ; S \text { neu } \\
P=P_1 \cup P_2 \cup\left\{S \rightarrow S_1 \mid S_2\right\}
\end{array}
\end{equation*}$$
(2)
$$\begin{equation*}
\begin{array}{l}
V=V_1 \cup V_2 \cup\{S\} ; S \text { neu } \\
P=P_1 \cup P_2 \cup\left\{S \rightarrow S_1 S_2\right\}
\end{array}
\end{equation*}$$
(3)
$$\begin{equation*}
\begin{array}{l}
V=V_1 \cup\{S\} ; S \text { neu } \\
P=P_1 \cup\left\{S \rightarrow \epsilon \mid S_1 S\right\}
\end{array}
\end{equation*}$$
(4) $$P=\left\{A \rightarrow \alpha^R \mid(A \rightarrow \alpha) \in P_1\right\}$$
---> Es folgt: Verallgemeinerte kontextfreie Grammatiken mit Produktionen der Gestalt $X \rightarrow r$, wobei $r$ ein regulärer Ausdruck über $(V \cup T)$ ist, erzeugen kontextfreie Sprachen.
