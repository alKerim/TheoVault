Präfix:
$u \preceq w \quad: \Leftrightarrow \quad \exists v . u v=w$

Anzahl der Vorkommen:
$\#_a(w):=\text { Anzahl der Vorkommen von } a \text { in } w$

Seien:
$A(w):=\#_{[}(w) \quad B(w):=\#_{]}(w)$

Wir nennen $w \in\{[,]\}^*$ balanciert gdw
(1) $A(w)=B(w)$ und
(2) für alle Präfixe $u$ von $w$ gilt $A(u) \geq B(u)$
- Balanciert: \[\], \[\[\]\], \[\] \[\], \[\[\[\] \[\]\] \[\]\]
- Nicht balanciert: ] \[, \[\]\]\[\[\]


# Satz
Die Grammatik $S \rightarrow \epsilon|[S]| S S$ erzeugt genau die Menge der balancierten Wörter.

[[Induktionsbeweis]]:
$u \in L_G(S) \Longrightarrow u$ balanciert:
Mit Ind. über die Erzeugung von $u$. (1) bewiesen, wir zeigen (2).
$$\begin{equation*}
\begin{array}{l}
\epsilon: p \preceq \epsilon \Longrightarrow p=\epsilon \Longrightarrow A(p)=B(p) \\
{[u]: \text { Sei } p \preceq[u]} \\
\text { Fall } p=\epsilon: A(p)=B(p) \\
\text { Fall } p=[u]: A(p)=A(u)+1=B(u)+1=B(p) \\
\text { Fall } p=[q \text { mit } q \preceq u \text { : } \\
A(p)=A(q)+1 \geq B(q)+1>B(q)=B(p) \\
\text { uv: Sei } p \preceq u v \text {. } \\
\text { Fall } p \preceq u: A(p) \geq B(p) \text { mit IA für } u \\
\text { Fall } p=u q \text { und } q \preceq v: \\
A(p)=A(u)+A(q)=B(u)+A(q) \geq B(u)+B(q)=B(u q)= \\
B(p)
\end{array}
\end{equation*}$$
$u$ balanciert $\Longrightarrow u \in L_G(S)$ :
Mit vollständiger Induktion über $n:=|u| .\left(\mathrm{dh} u=a_1 \ldots a_n\right)$
IA: Jedes balancierte Wort $<n$ liegt in $L_G(S)$.
Zz: $u \in L_G(S)$.
Falls $n=0$, so $u=\epsilon \in L_G(S)$.
Sei $n>0$.
Betrachte Werteverlauf von $h(w):=A(w)-B(w)$ :
$h(\epsilon), h\left(a_1\right), h\left(a_1 a_2\right), \ldots, h\left(a_1 \ldots a_n\right) \quad$ (alle $\geq 0!$ ).
Insb. gilt $a_1=\left[\right.$ und $\left.a_n=\right]$. Wir betrachten zwei Fälle:
- Es gibt nur die Nullstellen $h(\epsilon)$ und $h\left(a_1 \ldots a_n\right)$.
Dann ist $v:=a_2 \ldots a_{n-1}$ balanciert:
$$\begin{equation*}
\begin{array}{l}
\text { (1) } A(v)=A([v])-1=B([v])-1=B(v) \\
\text { (2) } p \preceq v: h([p)=A([p)-B([p)>0 \Longrightarrow \\
A(p)=A([p)-1>B([p)-1=B(p)-1 \Longrightarrow \\
A(p) \geq B(p) \\
\Longrightarrow v \in L_G(S)(\text { nach IA }) \Longrightarrow u=[v] \in L_G(S)
\end{array}
\end{equation*}$$
Es gibt noch eine Nullstelle $h\left(a_1 \ldots a_k\right)$.
Sei $u_1:=a_1 \ldots a_k, u_2:=a_{k+1} \ldots a_n$
Dann sind $u_1$ und $u_2$ balanciert:
$$\begin{equation*}
\text { (1) } \begin{array}{l} 
A\left(u_1\right)=B\left(u_1\right) \text { da } h\left(u_1\right)=0 ; \\
A\left(u_2\right)=A(u)-A\left(u_1\right)=B(u)-B\left(u_1\right)=B\left(u_2\right) \\
\text { (2) } p \preceq u_1 \Longrightarrow p \preceq u \Longrightarrow A(p) \geq B(p) \\
p \preceq u_2: A(p)=A\left(u_1 p\right)-A\left(u_1\right) \geq B\left(u_1 p\right)-B\left(u_1\right)=B(p) \\
\Longrightarrow u_1, u_2 \in L_G(S)\left(\text { nach IA, da }\left|u_i\right|<n\right) \\
\Longrightarrow u=u_1 u_2 \in L_G(S)
\end{array}
\end{equation*}$$
