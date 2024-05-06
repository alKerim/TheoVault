(1) Entferne alle von $q_0$ aus nicht [[erreichbar|erreichbaren]] Zustände.
(2) Berechne die äquivalenten Zustände des Automaten.
(3) Kollabiere den Automaten durch Zusammenfassung aller äquivalenten Zustände.

Zustände $p$ und $q$ sind unterscheidbar wenn es $w \in \Sigma^*$ gibt mit $\hat{\delta}(p, w) \in F$ und $\hat{\delta}(q, w) \notin F$ oder umgekehrt.
Zustände sind äquivalent wenn sie nicht unterscheidbar sind, d.h. wenn für alle $w \in \Sigma^*$ gilt:
$$\begin{equation*}
\hat{\delta}(p, w) \in F \quad \Leftrightarrow \quad \hat{\delta}(q, w) \in F
\end{equation*}$$
- Gilt $p \in F$ und $q \notin F$, dann sind $p$ und $q$ unterscheidbar.
- Sind $\delta(p, a)$ und $\delta(q, a)$ unterscheidbar, dann auch $p$ und $q$. $\Rightarrow$ Unterscheidbarkeit pflanzt sich rückwärts fort.

## Berechnung äquivalenter Zustände eines DFA
**Eingabe**: DFA $A=\left(Q, \Sigma, \delta, q_0, F\right)$
**Ausgabe**: Äquivalenzrelation auf $Q$.
**Datenstruktur**: Eine Menge $U$ ungeordneter Paare $\{p, q\} \subseteq Q$.
**Algorithmus U**:
1. $U:=\{\{p, q\} \mid p \in F \wedge q \notin F\}$
2. while $\exists\{p, q\} \notin U . \exists a \in \Sigma$. $\{\delta(p, a), \delta(q, a)\} \in U$ do $U:=U \cup\{\{p, q\}\}$
**Invariante**: $\{p, q\} \in U \Longrightarrow p$ und $q$ unterscheidbar

Am Ende gilt: $U$ ist Menge aller unterscheidbaren Zustandspaare.

##### Beweis:
$\{p, q\} \in U \Longrightarrow p$ und $q$ unterscheidbar:
Invariante $p$ und $q$ unterscheidbar $\Longrightarrow\{p, q\} \in U$ :
Induktion über die Länge eines unterscheidenden Worts.


#### Implementierung von $U$ :
Tabelle von anfangs unmarkierten Paaren $\{p, q\}, p \neq q$.
![[Screenshot 2024-05-06 at 14.58.10.png|150]]
**for all** $p \in F, q \in Q \backslash F$ do markiere $\{p, q\}$ 
**while** $\exists$ unmarkiertes $\{p, q\} \exists a \in \Sigma .\{\delta(p, a), \delta(q, a)\}$ ist markiert 
**do** markiere $\{p, q\}$
Komplexität:
$$\begin{equation*}
\left.O\binom{n}{2}+\binom{n}{2}\binom{n}{2}|\Sigma|\right)=O\left(\frac{n(n-1)}{2}+\frac{n^2(n-1)^2}{4}|\Sigma|\right)=O\left(n^4\right)
\end{equation*}$$
bei fixem $\Sigma$.

