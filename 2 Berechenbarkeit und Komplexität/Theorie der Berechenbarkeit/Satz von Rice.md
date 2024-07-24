Die von der TM $M_w$ berechnete Funktion bezeichnen wir mit $\varphi_w$. 
Wir betrachten implizit nur einstellige Funktionen.

#theo/basics 
Sei $F$ eine Menge [[berechenbar|berechenbarer]] Funktionen.
Es gelte weder $F=\emptyset$ noch $F=$ alle ber. Funkt. („F nicht trivial“) 
Dann ist [[unentscheidbar]], ob die von einer gegebenen TM $M_w$ berechnete Funktion Element $F$ ist, dh ob $\varphi_w \in F$.
____
==Warnung==
Es ist [[entscheidbar]], ob ein Programm
- länger als 5 Zeilen ist. Also das wäre formal $|w|=5$ 
- eine Zuweisung an die Variable $x_{17}$ enhält.
-> ==Alle nicht-triviale semantische Eigenschaften von Programmen sind unentscheidbar.== ^0f52a6

Valide nicht-triviale semantische Eigenschaften sind zB:
$\left\{w \in \Sigma^*:\left|\varphi_w(x)\right|=42\right.$ für alle $\left.x \in \mathbb{N}\right\}$
	Da wir $F$ definieren können als die Menge der Funktionen die eine Zeichenkette der Länge 42 zurückgeben.
	Da $F \not = \emptyset$  und $F$ obviously nicht die Menge aller ber. Funktionen ist gilt:
	$\varphi_{w}\in F$ ist unentscheidbar laut **Satz von Rice**.  

# Semantik nicht Syntax
#theo/basics 
Im Satz von Rice geht es um die von einem Programm berechnete Funktion ([[Semantics|Semantik]]), nicht um den Programmtext ([[Syntax]]).


_____
# Beispiele
### von Quiz Frage Q10.4. ( $z u$ H10.3)
Mehrfachauswahl. Sei $\Sigma:=\{0,1\}$. Auf welche der folgenden Sprachen lässt sich der Satz von Rice anwenden?
(a) $\left\{w \in \Sigma^*:\left|\varphi_w(x)\right|=42\right.$ für alle $\left.x \in \mathbb{N}\right\}$
	Da wir $F$ definieren können als die Menge der Funktionen die eine Zeichenkette der Länge 42 zurückgeben.
	Da $F \not = \emptyset$  und $F$ obviously nicht die Menge aller ber. Funktionen ist gilt:
	$\varphi_{w}\in F$ ist unentscheidbar laut **Satz von Rice**.  
(b) $\left\{w \in \Sigma^*:\left(\left|\varphi_w(x)\right|-5\right)^2 \geq 3\right.$ für alle $\left.x \in \mathbb{N}\right\}$
	ähnlich wie a)
(c) $\left\{w \in \Sigma^*:\left(\left|\varphi_w(x)\right|-5\right)^2=|w|\right.$ für alle $\left.x \in \mathbb{N}\right\}$
	Satz von Rice nicht anwendbar, da $|w|$ eine triviale semantische Eigenschaft ist, und diese Menge entscheidbar ist.
Lösung:
	a,b






______
# Gute Erklärung anhand beispiele
![[Screenshot 2023-07-15 at 18.45.21.png]]
Eigenschaft einer DTM M, die nur von L(M) abhängt.
Wenn $L(M)=L\left(M^{\prime}\right)$, dann:
Entweder $M$ und $M^{\prime}$ erfüllen es beide, oder keiner erfüllt es.

==markierte sind nicht-trivial==

**semantisch**
- ==Ist $L(M)$ regulär?==
- ==Ist $L(M)=\varnothing ?$==
- ==Ist $|L(M)| \geq 10$ ?
	- anders formuliert: Akzeptiert M mindestens 10 Worte?==
- Ist $L(M)$ Turing-erkennbar?
- Ist $L(M)$ überabzählbar unendlich?
- ==Ist $\mathrm{L}(\mathrm{M})=\{$ abrakadabra, moin $\}$ ?==
- ==Akzeptiert $\mathrm{M}$ alle Worte die mit a beginnen?==
=> mit $L(M)$ immer semantisch 

**nicht semantisch**
- Hat M mindestens 42 Zustände?
- Hält $M$ auf Eingabe $\varepsilon$ an?
- Überschreibt $M$ bei Eingabe abba jemals ein $\boldsymbol{\omega}$ ?


