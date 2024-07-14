Gegeben: Ungerichteter Graph $G=(V, E)$ und Zahl $k \in \mathbb{N}$.
Problem: Besitzt $G$ eine „Clique“ der Größe mindestens $k$ ?
Dh eine Teilmenge $V^{\prime} \subseteq V$ mit $\left|V^{\prime}\right| \geq k$ und alle $u, v \in V^{\prime}$ mit $u \neq v$ sind benachbart.

Beispiel mit 5-Clique:
![[Screenshot 2024-07-14 at 17.06.24.png|300]]
Anwendung von Clique-Berechnung:
Knoten $=$ Prozess
Kante $=$ Zwei Prozesse sind parallel ausführbar
$\Longrightarrow$ Clique ist Gruppe von parallelisierbaren Prozessen



# Komplexität
$C L I Q U E \in$ [[NP]]

CLIQUE ist [[NP-vollständig]].
Beweis: [[3KNF-SAT]] $\leq_p$ CLIQUE:
Eine [[Aussagenlogische Formel]] $F$ in 3KNF-SAT (oE: genau 3 Literale/Klausel)
$$\begin{equation*}
F=\left(z_{11} \vee z_{12} \vee z_{13}\right) \wedge \ldots \wedge\left(z_{k 1} \vee z_{k 2} \vee z_{k 3}\right)
\end{equation*}$$
wird auf einen Graphen abgebildet:
$$\begin{equation*}
\begin{aligned}
V & =\{(1,1),(1,2),(1,3), \ldots,(k, 1),(k, 2),(k, 3)\} \\
E & =\left\{\{(i, j),(p, q)\} \mid i \neq p \text { und } z_{i j} \neq \neg z_{p q}\right\}
\end{aligned}
\end{equation*}$$
$F$ ist [[erfüllbar]] durch eine Belegung $\sigma$
$\Longleftrightarrow$ Es gibt in jeder [[Klausel]] $i$ ein [[Literal]] $z_{i j_i}$ mit $\sigma\left(z_{i j_i}\right)=1$
$\Longleftrightarrow$ Die Literale $z_{1 j_1}, \ldots, z_{k j_k}$ sind paarweise nicht komplementär
$\Longleftrightarrow$ Die Knoten $\left(1, j_1\right), \ldots,\left(k, j_k\right)$ sind paarweise benachbart 
$\Longleftrightarrow$ $G$ hat eine Clique der Größe $k$.
$\square$

