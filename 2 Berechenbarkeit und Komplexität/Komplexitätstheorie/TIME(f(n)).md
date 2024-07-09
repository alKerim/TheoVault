Sei $f: \mathbb{N} \rightarrow \mathbb{N}$ eine [[total|totale]] Funktion.
Die Klasse der in Zeit $f(n)$ [[entscheidbar|entscheidbaren]] Sprachen:

$\operatorname{TIME}(f(n)):=\left\{A \subseteq \Sigma^* \mid\right.  \exists \operatorname{DTM} M . A=L(M) \wedge  \left.\forall w \in \Sigma^* . \operatorname{time}_M(w) \leq f(|w|)\right\}$

Anmerkungen:
- $n$ ist implizit die Länge der Eingabe $w$
- Die [[DTM]] entscheidet die Sprache $A$ in $\leq f(n)$ Schritten
- Related: [[time_M(w)]]

==**Für Verständnis**==:
- $\operatorname{TIME}$ ist eine Menge von Sprachen (Menge von Mengen)
	- Für jede dieser Sprachen $A$ gilt: 
		- $\exists \operatorname{DTM} M.$ mit 
			- $L(M) = A$
			- und $\forall w \in \Sigma^*$ muss die (Anzahl Schritte bis $M[w]$ hält) $\leq f(|w|)$ ) 
				formal: [[time_M(w)]]. $\operatorname{time}_{M(w)}\leq f(|w|)$ 




# Für Polynome
Wir betrachten Polynome mit Koeffizienten $a_k, \ldots a_0 \in \mathbb{N}$ :
$p(n)=a_k n^k+\cdots+a_1 n+a_0$

$$\begin{equation*}
\mathrm{P}:=\bigcup_{p \text { Polynom }} \operatorname{TIME}(p(n))
\end{equation*}$$
(Mit $P$ ist dieses [[P]] gemeint.)
Damit gilt auch
$$\begin{equation*}
\mathrm{P}=\bigcup_{k \geq 0} \operatorname{TIME}\left(O\left(n^k\right)\right)
\end{equation*}$$
wobei
$$\begin{equation*}
\operatorname{TIME}(O(f)):=\bigcup_{g \in O(f)} \operatorname{TIME}(g)
\end{equation*}$$
Verständnis:
- $g$ ist ein polynom, mit Komplexität $O(f)$
- $\bigcup_{g \in O(f)}$ sind ==ALLE POLYNOME== mit Komplexität $O(f)$
- $\bigcup_{g \in O(f)} \operatorname{TIME}(g)$ sind ==ALLE SPRACHEN== die mind. eine DTM $M$ haben, die die Sprache mit Komplexität $O(f)$ erkennt. 
	- Also falls $f=n^2$, dann $\forall w \in \Sigma^*$ hält $L[M]$ in unter $n^2$ Schritten
	- Anders formuliert: Alle Sprachen, die $\leq n^2$ Schritten erkannt/entschieden werden.


# Schreibweise für Verständnis
Man kann schreiben
$\operatorname{TIME}\left(O\left(n^2\right)\right) \subseteq \mathrm{P}$
Weil:
- $P$ sind alle die von einer [[DTM|DTM]] in polynomieller Zeit lösbaren Probleme
- $\operatorname{TIME}\left(O\left(n^2\right)\right)$ ist die Menge aller Sprachen die in unter $n^2$ erkannt werden.

# Zeit
#theo/zeit 
#theo/cheatsheet 
Bemerkungen
- $O(n \log n) \subset O\left(n^2\right)$
- $n^{\log n}, 2^n \notin O\left(n^k\right)$ für alle $k$
- Beweis $A \notin \mathrm{P}$ meist schwierig #theo/wichtig 
- Warum $\mathrm{P}$ und nicht $(\mathrm{zB}) O\left(n^{17}\right)$ ? 
	Um robust bzgl Maschinenmodell zu sein:
	==1-Band DTM braucht $O\left(t^2\right)$ Schritte um $t$ Schritte einer $k$-Band DTM zu simulieren.==
	Fast alle bekannten ,vernünftigen“ Maschinenmodelle lassen sich von einer DTM in polynomieller Zeit simulieren.
	Offen: Quantencomputer


# Beispiele
- $\left\{w w^R \mid w \in \Sigma^*\right\} \in \operatorname{TIME}\left(O\left(n^2\right)\right) \subseteq \mathrm{P}$
- $\{(G, w) \mid G$ ist CFG $\wedge w \in L(G)\} \in \mathrm{P}$
- $\{(G, w) \mid G$ ist Graph $\wedge w$ ist Pfad in $G\} \in \mathrm{P}$
- $\{b i n(p) \mid p$ Primzahl $\} \in \mathrm{P}$

Beweis durch Angabe eines Algorithmus mit Komplexität $O\left(n^k\right)$.

