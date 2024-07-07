- [[Mengentheoretischer Ausdruck]]
- [[Reflexiv transitive Hülle]]


- $L \subseteq L_1 \Rightarrow L \cap \bar{L_1}$

#theo/basics
- Für alle Sprachen $A, B, C$ gilt $(A \backslash C) B=A B \backslash C B$.
	Die Aussage ist falsch. Sei $A=\{a a\}, B=\{\epsilon, a\}$ und $C=\{ aaa \}$. 
	Dann gilt $(A \backslash C) B=\{ aa, aaaa \}$ und $A B \backslash C B=\{a a\}$.




PDA -> CFG (Algorithmus aus VL). PDA mit n Zuständen. Wie zB. 
	$n^2 k+1 \quad V=Q \times \Gamma \times Q \cup\{S\}$ (s. Folie 200)




# Folgende Aussagen sind äquivalent:
- $A$ ist [[semi-entscheidbar (s-e)|semi-entscheidbar]]
- $A$ ist [[rekursiv aufzählbar]]
- $\chi_A^{\prime}$ ist [[berechenbar]]
- $A=L(M)$ für eine TM $M$
- $A$ ist Definitionsbereich einer berechenbaren Funktion
- $A$ ist Wertebereich einer berechenbaren Funktion


# $\Sigma^*$ Hack
2/3. [[Reduktion]] von [[Postsche Korrespondenzproblem - PCP|PCP]] Instanz auf $G_4:={ }_{,} \overline{G_1} \cup \overline{G_2}$ “. 
Instanz unlösbar $\Rightarrow L\left(G_1\right) \cap L\left(G_2\right)=\emptyset$
$\Rightarrow L\left(G_4\right)=\Sigma^* \Rightarrow L\left(G_4\right)$ reg/det.


