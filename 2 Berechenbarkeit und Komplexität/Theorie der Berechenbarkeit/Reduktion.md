#theo/definition
# reduzierbar
![[reduzierbar]]

# Die Reduktion
#theo/basics/reduktion 
Wir schreiben dann $A \leq B$. 
"$A$ lässt sich auf $B$ reduzieren"

Intuition:
- Aus einem Algorithmus für $B$ kann man einen Algorithmus für $A$ gewinnen.
- Ist $B$ [[entscheidbar]], dann erst recht $A$.
- Ist $A$ [[unentscheidbar]], dann auch $B$.
- $B$ ist mindestens so schwer zu lösen wie $A$.


# Entscheidbarkeit
Falls $A \leq B$ und $B$ ist entscheidbar, so ist auch $A$ entscheidbar.

#### Beweis
Beweis:
Es gelte $A \leq B$ mittels $f$ und $\chi_B$ sei [[berechenbar]]. Dann ist $\chi_B \circ f$ berechenbar und $\chi_A=\chi_B \circ f$ :
$$\begin{equation*}
\chi_A(x)=\left\{\begin{array}{ll}
1, & x \in A \\
0, & x \notin A
\end{array}=\left\{\begin{array}{ll}
1, & f(x) \in B \\
0, & f(x) \notin B
\end{array}=\chi_B(f(x))\right.\right.
\end{equation*}$$

# Untentscheidbarkeit
Falls $A \leq B$ und $A$ ist [[unentscheidbar]], dann ist auch $B$ unentscheidbar.


# Beispiele
#### Beispiel 1 (aus VL)
Wir haben A auf B reduziert
![[Screenshot 2024-06-20 at 15.12.38.png|500]]

#### Beispiel 2
Da $K \leq H$ (mit Reduktion $f(w):=w \# w$ ) und $K$ [[unentscheidbar]] ist, ist auch $H$ unentscheidbar.

###### von tweedback:
Beim Halteproblem auf leerem Band: Ich verstehe nicht, warum man das Programm ohne Eingabe auf ein Programm mit Eingabe reduzieren kann. Ändert das nicht die Semantik des Programms?

Antwort:
	Ich verstehe die Frage nicht ganz. In beiden Fällen haben wir doch eine Eingabe? Im ersten Fall ist es die Kodierung der TM selbst und im zweiten Fall ist es das leere Wort.



# Templates
### (Ist $L\left(G_1\right) \subseteq L\left(G_2\right)$?) $\leq$ Ist ($L\left(G_1\right)=L\left(G_2\right)$?)
[Ü11.3 a)](https://teaching.model.in.tum.de/2024ss/theo/ex/ue11-nosolution.pdf?key=wzjSitSL), [Lösung von Adrian](https://zulip.in.tum.de/user_uploads/2/13/BBJjE0eoqAU8b3ukjozU4Nme/Theo-S11.pdf):
$\langle 3\rangle$ Ist $L\left(G_1\right) \subseteq L\left(G_2\right)$ ?
$\langle 4\rangle$ Ist $L\left(G_1\right)=L\left(G_2\right)$ ?
Reduktion
	Für $G_1^{\prime}$ und $G_2^{\prime}$ roll gelten
	$$\begin{equation*}
	\begin{aligned}
	L\left(G_1^{\prime}\right)= & L\left(G_1\right) \cup L\left(G_2\right) \quad L\left(G_2^{\prime}\right)=L\left(G_2\right) \\
	& \left(G_1, G_2\right) \in\langle 3\rangle \\
	\Leftrightarrow & L\left(G_1\right) \leq L\left(G_2\right) \\
	\Leftrightarrow & L\left(G_1\right) \cup L\left(G_2\right)=L\left(G_2\right) \\
	\Leftrightarrow & L\left(G_1^{\prime}\right)=L\left(G_2^{\prime}\right) \\
	\Leftrightarrow & \left(G_1^{\prime}, G_2^{\prime}\right) \in\langle 4\rangle \\
	\Leftrightarrow & f\left(G_1^{\prime}, G_2^{\prime}\right) \in\langle 4\rangle
	\end{aligned}
	\end{equation*}$$
### (Ist $L\left(G_1\right) \cap L\left(G_2\right)=\emptyset$ ?) $\leq$ (Ist $\left|L\left(G_1\right) \cap L\left(G_2\right)\right|<\infty$ )
[Ü11.3 b)](https://teaching.model.in.tum.de/2024ss/theo/ex/ue11-nosolution.pdf?key=wzjSitSL), [Lösung von Adrian](https://zulip.in.tum.de/user_uploads/2/13/BBJjE0eoqAU8b3ukjozU4Nme/Theo-S11.pdf):
$\langle 1\rangle$ Ist $L\left(G_1\right) \cap L\left(G_2\right)=\emptyset$ ?
$\langle 2\rangle$ Ist $\left|L\left(G_1\right) \cap L\left(G_2\right)\right|<\infty$ ?
Reduktion:
	$\begin{aligned} L\left(G_1^{\prime}\right)= & L\left(c^*\right) L\left(G_1\right) \quad L\left(G_2^{\prime}\right)=L\left(c^*\right) L\left(b_2\right) \\ & \left(G_1, G_2\right) \in\langle 1\rangle \\ \Rightarrow & L\left(G_1\right) \cap L\left(G_2\right)=\varnothing \\ \Leftrightarrow & \left|L\left(c^*\right)\left(L\left(G_1\right) \cap L\left(G_2\right)\right)\right|<\infty \\ \Rightarrow & \left|L\left(G_1^{\prime}\right) \cap L\left(G_2^{\prime}\right)\right|<\infty \\ \Rightarrow & f\left(b_1, G_2\right) \in\langle 2\rangle\end{aligned}$



# Cheatsheet Strategien
- Verschiedene Typen von Reduktionen aufs Cheatsheets


# Denk Strategien
wenn ein w in A ist, dann soll es auch in B sein 
wenn ein w nicht in A ist, dann soll es auch nicht in B sein 
oder
wenn ein w in A ist, dann soll es nicht in B sein

- Gadgets: wie bilde ich eine Klausel ab, 
	- kleinere strukturen herzuleiten die zb eine Klausel darstellen
	- dazu nochmal auf HA12 schauen


- Edge Cases nicht vergessen 

- auf hilfsblatt mit reduktionen rumprobieren, damit man auf die richtige idee kommt