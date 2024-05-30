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



# Fragen:
1. Wie sähe ein Beispiel aus, bei dem wir die Eigenschaft von des $uv^iwx^iy$ nutzen gegenüber dem $uv^iw$ haben, also die Eigenschaft nutzen, dass die Zerlegung zwei Variablen haben die wir Pumpen können?