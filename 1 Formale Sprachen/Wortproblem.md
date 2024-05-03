Gegeben: eine Grammatik $G$, ein Wort $w \in \Sigma^*$ 
Frage: Gilt $w \in L(G)$ ?
____
Sei $D$ ein DFA, NFA, RE, rechtslineare Grammatik ....
Wortproblem: Gegeben $w$ und $D$, gilt $w \in L(D)$ ?
___

Spoiler: [[Automat|Automaten]] lösen das Wortproblem!!!

- In den kommenden Wochen untersuchen wir das Wortproblem für Grammatiken vom Typ 3 und Typ 2.
- Wir studieren Algorithmen, die für eine gegebene [[Grammatik]] $G$ einen [[Automat|Automaten]] $A_G$ konstruieren, und untersuchen ihre Laufzeit. 

$A_G$ ist eine abstrakte Beschreibung eines Programms zur Lösung des Wortproblems.


Der Algorithmus mit $G$ als Eingabe und $A_G$ als Ausgabe ist eine abstrakte Beschreibung eines Programms für die automatische Synthese von [[Recognizer|Recognizern]] ([[lex & yacc]]).


