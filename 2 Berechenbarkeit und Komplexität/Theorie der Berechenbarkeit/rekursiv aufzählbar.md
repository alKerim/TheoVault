Typ-0 Sprachen in der [[Chomsky-Hierarchie]].

Die von [[Turingmaschine - TM|Turingmaschinen]] akzeptierten Sprachen sind genau die [[Chomsky-Hierarchie#^2fe2b9|Typ-0-Sprachen]] der [[Chomsky-Hierarchie]].
	Beweis:
	Wir beschreiben nur die Beweisidee. (Mehr Details: \[Schöning\]).
	"$\Longrightarrow$": Grammatikregeln können direkt die Rechenregeln einer TM simulieren.
	"$\Longleftarrow$": Die (nichtdeterministische) TM versucht von ihrer Eingabe aus das Startsymbol der Grammatik zu erreichen, indem sie die Produktionen der Grammatik von rechts nach links anwendet, ([[Nichtdeterminismus|nichtdeterministisch]]) an jeder möglichen Stelle.


# gdw's
- Eine Menge A ist **rekursiv aufzählbar** gdw sie [[semi-entscheidbar (s-e)|semi-entscheidbar]] ist.
	Beweis: [[theo-folien-handout.pdf#page=283]]



# Formale Definition
Eine Menge $A$ heißt **rekursiv aufzählbar** (recursively enumerable) 
gdw 
- $A=\emptyset$ 
oder 
- es eine [[berechenbar|berechenbare]] [[total|totale]] Funktion $f: \mathbb{N} \rightarrow A$ gibt, so dass
$$\begin{equation*}
A=\{f(0), f(1), f(2), \ldots\}
\end{equation*}$$

Bemerkung:
- Es dürfen Elemente doppelt auftreten $(f(i)=f(j)$ für $i \neq j$ )
- Die Reihenfolge ist beliebig.


==Warnung: Rekursiv aufzählbar $\neq$ [[abzählbar]]!==
- Rekursiv aufzählbar $\Longrightarrow$ [[abzählbar]]
- Aber nicht umgekehrt: jede Sprache ist abzählbar aber nicht jede Sprache ist rekursiv aufzählbar (s.u.)


