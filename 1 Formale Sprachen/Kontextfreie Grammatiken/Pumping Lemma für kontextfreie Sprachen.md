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


# Visualisiert:
![[Screenshot 2024-05-27 at 14.38.10.png|450]]

# Mit PL zeigbar nicht-kontextfrei
$L=\{ww\quad|\quad w\in\Sigma^{*}\}$
$L=\{a^nb^nc^n|n\in N\}$

 

 
______
# Beispiele
### Beispiel 1
$L=\{a^nb^nc^n\|n\in N\}$
aaabbbccc

vwx = aaa | abb | bbb | bcc | ccc


### Beispiel 2
Mit dem Pumping-Lemma kann man zeigen, dass die Sprache $\left\{w w \mid w \in\{a, b\}^*\right\}$ nicht kontextfrei ist.
Dies zeigt, dass Kontextbedingungen in Programmiersprachen, etwa "Deklaration vor Benutzung", nicht durch kontextfreie Grammatiken ausgedrückt werden können.



# Fragen:
1. Wie sähe ein Beispiel aus, bei dem wir die Eigenschaft von des $uv^iwx^iy$ nutzen gegenüber dem $uv^iw$ haben, also die Eigenschaft nutzen, dass die Zerlegung zwei Variablen haben die wir Pumpen können?