Eine [[Kontextfreie Grammatiken|kontextfreie Grammatik]] $G$ ist in Chomsky-Normalform **gdw** alle Produktionen eine der Formen ^e1cf46
$$\begin{equation*}
A \rightarrow a \text { oder } A \rightarrow B C
\end{equation*}$$
haben.

# Edge-Case $\epsilon$
Wer auf $\epsilon \in L\left(G^{\prime}\right)$ nicht verzichten möchte:
Füge am Ende $S^{\prime} \rightarrow S, S^{\prime} \rightarrow \epsilon$ hinzu und setze $S^{\prime}$ als Startsymbol.



# Fakten
Zu jeder CFG $G$ kann man eine CFG $G^{\prime}$ in Chomsky-Normalform konstruieren mit $L\left(G^{\prime}\right)=L(G) \backslash\{\epsilon\}$.  #theo/wichtig 


Äquivalenz von Grammatiken: Zwei Grammatiken sind nicht äquivalent, nur wenn sie die gleiche Sprache erzeugen. Grammatiken sind äquivalent, wenn alles gleich ist an ihnen.


# CNF-Algorithmus
[[CNF-Algorithmus]]


# Beispiele
### Beispiel 1: Loop finding Trick

^4d8aff

Hier eine gute Art und Weise herauszufinden ob ein Loop existiert. Einfach die Relationen in einem Graph zeichnen. #theo/trick
![[Screenshot 2024-05-23 at 15.08.29.png]]




_____
Related: Wurde von [[Noam Chomsky]] entworfen.