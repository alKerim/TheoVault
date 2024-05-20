Die Residual[[sprache]] von $L$ bzgl. $w \in \Sigma^*$ ist die Menge
$$\begin{equation*}
L^w:=\left\{z \in \Sigma^* \mid w z \in L\right\} .
\end{equation*}$$
$L^{\prime} \subseteq \Sigma^*$ ist Residualsprache von $L$ wenn es $w$ gibt mit $L^{\prime}=L^w$.


# Fakten
- Jeder [[Kanonischer Minimalautomat|minimaler DFA]] für eine reguläre Sprache $L$ unterscheidet sich vom kanonischen Minimalautomaten $M_L$ nur durch eine Umbenennung der Zustände.

# GENAU DANN WENNs
$uw \in L \Leftrightarrow w \in L^u$
___
Sei $p:=\hat{\delta}\left(q_0, u\right)$ und $q:=\hat{\delta}\left(q_0, v\right)$. Es gilt:
$p \equiv_M q \quad \Leftrightarrow \quad L_M(p)=L_M(q)$
		$\Leftrightarrow \quad \forall w \in \Sigma^* . \hat{\delta}(p, w) \in F \Leftrightarrow \hat{\delta}(q, w) \in F$
		$\Leftrightarrow \quad \hat{\delta}\left(q_0, u w\right) \in F \Leftrightarrow \hat{\delta}\left(q_0, v w\right) \in F$
		$\Leftrightarrow \quad \forall w \in \Sigma^* . u w \in L \Leftrightarrow v w \in L$
		$\Leftrightarrow \quad \forall w \in \Sigma^* . w \in L^u \Leftrightarrow w \in L^v$
		$\Leftrightarrow \quad L^u=L^v$
		$\Leftrightarrow \quad u \equiv_L v$
Intuition:
- Nicht-äquivalente Wörter führen zu nicht-äquivalenten Zuständen.
- Nicht-äquivalente Zustände werden von nicht-äquivalenten Wörtern erreicht.
____

# Beobachtungen
![[Screenshot 2024-05-13 at 14.29.16.png]]
_____
Sei $\mathcal{R}_L$ die Menge der Residualsprachen von $L$.
Definition 3.58 (Kanonischer Minimalautomat)
$$\begin{equation*}
M_L:=\left(\mathcal{R}_L, \Sigma, \delta_L, L, F_L\right)
\end{equation*}$$
mit $\delta_L(R, a):=R^a$ und $F_L:=\left\{R \in \mathcal{R}_L \mid \epsilon \in R\right\}$.
$\delta_L$ ist wohldefiniert und $\hat{\delta}_L(R, w)=R^w$. Jeder Zustand $R$ erkennt die Sprache $R$ und somit $L\left(M_L\right)=L$.

$R_{L}= \{L_1,L_2,L_3,L_4\}$
------>> Also hierbei gilt für jede Residualsprache $L_x$: sobald $\epsilon \in L_x$ dann ist $L_x$ ein Endzustand.
	Nun also, es kann mehrere Endzustände geben, lass dich hier nicht verwirren, $\epsilon$ steht hierbei nicht für den Startzustand sondern, weil 


# Regeln zum Residual-Beweisen
![[IMG_4416.jpg]]

$L^b=\left\{w \in \Sigma^* \mid \text { bw } \in L\right\}=\varnothing$

Allgemein für $\Sigma=\{a, b\}$ and eine beliebige Sprache $L$
$\underbrace{L^w}_{wz}=\{a\} \underbrace{L^{wa}}_{waz} \cup\{b\} \underbrace{L^{wb}}_{wbz} \underbrace{(\cup \{\epsilon \})}_{\text{falls } w \in L} =$
By the way:
$L^{wa}= \left(L^w\right)^a$
$L^{wb}=\left(L^w\right)^b$


![[IMG_9905.jpg]]




# Beispiele
### Beispiel zur Schreibweise
![[Screenshot 2024-05-13 at 14.13.48.png|400]]
Beschreibung der obigen Sprache des DFAs
$\{a\}L_{1}\cup \{b\}L_2 \cup \{\epsilon\}$


### Beispiel 2
$L = \{a^{n}b^{n}|n \in N\}$
$L^{a}= \{w\in \Sigma^{*}| aw \in L\} = \{a^{n}b^{n+1}| n \in N\}$
$L^{aaa}= \{w\in \Sigma^{*}| aaaw \in L\} = \{a^{n}b^{n+3}| n \in N\}$
$L^{aab}= \{w\in \Sigma^{*}| aabw \in L\} = \{b\}$
$L^{b}= \{w\in \Sigma^{*}| bw \in L\} = \emptyset$




# Aufgabentypes
vielleicht rüberkopieren: [[1. Theo Zusammenfassung#Type A: Sprache gegeben]]
