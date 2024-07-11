Beweisen von Rekursiven Funktionen auf Rekursiven Ausdrücken
# Struktur

| $\operatorname{empty}(\emptyset)=$             | $\operatorname{empty}(\alpha \beta)=$        |
| ---------------------------------------------- | -------------------------------------------- |
| $\operatorname{empty}(\mathrm{a})=$            | $\operatorname{empty}(\alpha \mid \beta)=$   |
| $\operatorname{empty}(\boldsymbol{\epsilon})=$ | $\operatorname{empty}\left(\alpha^*\right)=$ |


# Algorithmus (Induktionsbeweis) - Beispiel
![[Pasted image 20240705134232.png]]
![[Screenshot 2024-07-05 at 13.44.12.png]]


# Important Rules:
#theo/cheatsheet 
- $\forall w$ in $L$, gilt Eigenschaft blablabla,.... $eigenschaft(\emptyset)=true$ 
  weil es gibt in $\emptyset$ keine Wörter für die die **Eigenschaft nicht gilt**
- $\exists w$ in $L$, für das gilt Eigenschaft blablabla,.... $eigenschaft(\emptyset)=false$ 
  weil es gibt in $\emptyset$ keine Wörter für die die **Eigenschaft gilt**



# Aufgaben
Harte ABER GUTE Aufgabe: [H2.6](https://teaching.model.in.tum.de/2024ss/theo/ex/ue02-solution.pdf?key=Fvnz2LI1)



# Beweis Mittels Struktureller Induktion
#theo/beweis 
[[Beweis Types#$L(G) subseteq L$]]
[[Beweis Types#$L subseteq L(G)$]]
