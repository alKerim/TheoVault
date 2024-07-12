Eine CFG $G$ heißt mehrdeutig 
**gdw**
es ein $w \in L(G)$ gibt, das zwei verschiedene Syntaxbäume hat, also zwei verschiedene [[Syntaxbaum|Syntaxbäume]] mit Wurzel $S$ und Rand $w$.

![[Screenshot 2024-05-23 at 15.07.55.png]]
# Beispiele
#### Beispiel 1: nicht inhärent
Die Grammatik $E \rightarrow E+E|E * E|(E) \mid a$ ist mehrdeutig betrachte $a+a * a$. Die erzeugte Sprache ist aber nicht [[inhärent mehrdeutig]] (siehe Beispiel Arithmetische Ausdrücke).


# Side Facts
#### Nur Grammatiken sind mehrdeutig
Nur Grammatiken sind mehrdeutig. 
Sprachen (zB [[Kontextfreie Grammatiken|kontextfreie Sprachen]]) können nicht mehrdeutig sein, sondern nur [[inhärent mehrdeutig]]



# Beweisen dass nicht mehrdeutig (=[[eindeutig]])
[HA6.4](https://teaching.model.in.tum.de/2024ss/theo/ex/ha06-solution.pdf?key=DOuuxWLm)
Schritte:
Wir zeigen, dass $G$ [[eindeutig]] ist, indem wir 
- für jedes Nichtterminal $X \in\{E, T, F\}$ und jedes Wort $w \in L_G(X)$ einen eindeutigen ersten Schritt in einem Syntaxbaum von $w$, das mit $X$ beginnt, angeben, d.h. eine eindeutige Produktion $X \rightarrow \beta$ und eindeutige Teilwörter von $w$ für jedes Nichtterminal in $\beta$. 
- Da ein Syntaxbaum eines Wortes $w \in L(G)$ mit $E$ anfängt und jeder Schritt von einem Syntaxbaum zu Terminalen und zu Syntaxbäumen, die mit Nichtterminalen beginnen, führt, folgt daraus, dass der Syntaxbaum jedes Wortes eindeutig ist.
Für genaueres siehe Lösung der HA im Link oben.


______
Related: [[inhärent mehrdeutig]]