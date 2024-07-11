Ähnlich zum [[Pumping Lemma#Pumping Lemma für reguläre Sprachen]]

Definition: [[Kontextfreie Sprache]]

# Formale Definition
Für jede kontextfreie Sprache $L$ gibt es ein $n \geq 1$, so dass sich jedes Wort $z \in L$ mit $|z| \geq n$ zerlegen lässt in
	$z=u v w x y$
mit
- $v x \neq \epsilon$,
- $|v w x| \leq n$, und
- $\forall i \in \mathbb{N} . u v^i w x^i y \in L$.


# Nicht-Kontextfrei
Es gibt ein $n \geq 1$, sodas für jede Zerlegung $z$ die Bedingung nicht gilt.
	bzw. dass es keine Zerlegung $z$ gibt für die alle Bedingungen gelten.


# Visualisiert:
![[Screenshot 2024-05-27 at 14.38.10.png|450]]

# Mit PL zeigbar, dass nicht-kontextfrei
$L=\{ww\quad|\quad w\in\Sigma^{*}\}$
$L=\{a^nb^nc^n|n\in N\}$


# Template für Aufgaben
TODO
Angenommen L wäre kontextfrei. Dann müsste sie das Pumping-Lemma für kontextfreie Sprachen erfüllen.
z.z.: $L$ erfüllt das PL nicht

Sei $n$ eine beliebige PL-Zahl
Wähle $z= ...$ $\in L$ 
Sei $z=uvwxy$ eine Zerlegung, die die Pl-Eigenschaften erfüllt.

Fallunterscheidung:
$|vx|$ enthält...
- Nur a's
- a's und b's
- Nur b's
- b's und c's
- Nur c's

Man kann nun diese Fälle entweder einzeln behandeln oder man fasst sie zusammen in 2 größere Fälle:
- enthält a's
	- Nur a's
	- a's und b's
- keine a's
	- Nur b's
	- b's und c's
	- Nur c's


# Template Beispielaufgabe (Endterm23)
#theo/cheatsheet 
a)* Zeigen Sie unter Verwendung des Pumpinglemmas, dass folgende Sprache über dem Alphabet $\Sigma:=\{a, b\}$ nicht kontextfrei ist: $L:=\left\{a^i b^j a^k \mid i, j, k \in \mathbb{N} \wedge j=\min (i, k)\right\}$.

- Wir nehmen an, dass $L$ kontextfrei ist und leiten einen Widerspruch her.
- Sei $n \in \mathbb{N}_{+}$eine Pumping-Lemma-Zahl für $L$.
- Wähle $z:=a^n b^n a^n \in L$, es gilt $|z|=3 n \geq n$.
- Es gibt also für $z$ eine Zerlegung $z=u v w x y$ mit den Eigenschaften
	1. $v x \neq \varepsilon$
	2. $|v w x| \leq n$
	3. $\forall i \in \mathbb{N}$. $u v^i w x^i y \in L$.
- Wir unterscheiden die folgenden Fälle:
	- $|v x|_a=0$ : Aus (1) und der Wahl von $z$ folgt, dass $|v x|_b=k>0$. Folglich ist $u v^0 w x^0 y=$ $a^n b^{n-k} a^n \notin L$, da $n-k \neq \min (n, n)$. Dies ist ein Widerspruch zu (3)
	- $|v x|_a=k>0$ : Wir machen eine weitere Fallunterscheidung:
		- $|v x|_b=0$ : 
			Dann ist $u v^0 w x^0 y=a^{n-k} b^n a^n$ oder $u v^0 w x^0 y=a^n b^n a^{n-k}$. 
			Da $\min (n-k, n) \neq n$ beziehungweise $\min (n, n-k) \neq n$ und daher $u v^0 w x^0 y \notin L$ folgt wieder ein Widerspruch zu (3).
		* $|v x|_b=l>0$. 
			Wegen (2) berührt $vwx$ nur einen der $a$ Blöcke. 
			$u v^2 w x^2 y$ hat daher die Form $a^{n+k} b^{n+l} a^n$ oder $a^n b^{n+l} a^{n+k}$. 
			Da $k, l>0$ sind auch $n+k>n$ und $n+l>n$. Folglich ist die Anzahl der $b$'s $(n+l)$ größer als $\min (n+k, n)=\min (n, n+k)=n$. 
			Daher ist $u v^2 w x^2 y \notin L$, ein Widerspruch zu (3).
- Jeder Fall führt zu einem Widerspruch. Somit ist $L$ nicht kontextfrei.
 
______
# Beispiele
### Beispiel 1
$L=\{a^nb^nc^n\|n\in N\}$
aaabbbccc

vwx = aaa | abb | bbb | bcc | ccc

Fallunterscheidung hier:
- nur a's
- a's und b's
- nur b's
- b's und c's
- c's

### Beispiel 2
Mit dem Pumping-Lemma kann man zeigen, dass die Sprache $\left\{w w \mid w \in\{a, b\}^*\right\}$ nicht kontextfrei ist.
Dies zeigt, dass Kontextbedingungen in Programmiersprachen, etwa "Deklaration vor Benutzung", nicht durch kontextfreie Grammatiken ausgedrückt werden können.


### Beispiel 3: schwer
(H6.3)
An der Technischen Hochschule Estlingen-Oberfeld werden Matrikelnummern nach einem kuriosen System vergeben: Matrikelnummern müssen Zahlen sein, deren Quersumme eine Primzahl ist, eine alte Estlinger Tradition. Nun hält der technische Wandel auch nicht vor Estlingen-Oberfeld ein, und der Rektor versucht verzweifelt, eine kontextfreie Grammatik zu finden, die alle korrekten Matrikelnummern erzeugt.

Sei $\Sigma:=\{0, \ldots, 9\}$. Zeigen Sie, dass die Sprache $L:=\left\{w \in \Sigma^*: \sum_{i \geq 1} w_i\right.$ prim $\}$ nicht kontextfrei ist.

Lösungsskizze. Wir wenden das Pumping-Lemma für kontextfreie Sprachen an. Sei also $n \in \mathbb{N}$ beliebig. Wir wählen das Wort $z:=1^p$, wobei $p \geq n$ eine Primzahl ist. Nun erhalten wir eine Zerlegung $z=u v w x y$. Sowohl $v$ als auch $x$ enthalten nur das Zeichen 1 , somit gilt $v x=1^k$ für $k:=|v x|$. Sei nun $i:=1+p$. Wir erhalten
\begin{equation*}
u v^i w x^i y=1^{p+k p}
\end{equation*}

Da aber $p+k p=p(k+1)$ und $k>0$ nach den Eigenschaften der Zerlegung gilt, besitzt $p(k+1)$ mindestens zwei Teiler ( $p$ und $k+1$ ), ist keine Primzahl, und $u v^i w x^i y \notin L$.

In beiden Fällen haben wir ein $i$ gefunden, sodass $u v^i w x^i y \notin L$. Damit gilt die Eigenschaft des PL nicht, und $L$ kann nicht kontextfrei sein.

# Fragen:
1. Wie sähe ein Beispiel aus, bei dem wir die Eigenschaft von des $uv^iwx^iy$ nutzen gegenüber dem $uv^iw$ haben, also die Eigenschaft nutzen, dass die Zerlegung zwei Variablen haben die wir Pumpen können?
