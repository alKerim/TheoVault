Zum überführen von einer Grammatik in [[Chomsky-Normalform]].

# Schritte
#### 1: Entfernen von Terminalen in langen Produktionen
$A \rightarrow aB$
zu
$A \rightarrow X_aB$
$X_a \rightarrow a$

#### 2: Entfernen langer Produktionen
$S \rightarrow ASA$
zu
$S \rightarrow AX_{SA}$
$X_{SA} \rightarrow SA$

#### 3: Entfernen $\epsilon$-Produktionen
1. Entfernen der ersten $B \rightarrow \epsilon$ Produktion
2. Schauen alle Vorkommnisse von $B$ und dann $B$ durch $\epsilon$ ersetzen
	a. zB $A \rightarrow CB$ wird zu $A \rightarrow C$
	b. zB $C \rightarrow B$ wird zu $C \rightarrow \epsilon$.
		 In diesem Fall dann wieder zu Schritt 2. und das gleiche mit $C$ machen



#### 4: Entfernen von Kettenproduktionen
Wir nennen $A \rightarrow B$ eine Kettenproduktion. [[theo-folien-handout.pdf#page=163&selection=0,0,8,22|Satz aus VL]]

Edge Cases: #theo/wichtig 
- $S \rightarrow S$ darf man löschen 


