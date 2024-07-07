Gegeben: eine Grammatik $G$, ein Wort $w \in \Sigma^*$ 
Frage: Gilt $w \in L(G)$ ?
____
Sei $D$ ein [[DFA - Deterministische endliche Automaten|DFA]], [[NFA - Nichtdeterministische endliche Automaten|NFA]], [[RE - Reguläre Ausdrücke|RE]], [[Rechtslineare Grammatiken|rechtslineare Grammatik]] ....
**Wortproblem**: Gegeben $w$ und $D$, gilt $w \in L(D)$ ?
___

Spoiler: 
- [[Automat|Automaten]] lösen das Wortproblem für [[Reguläre Sprachen]]!!!
- [[CYK Algorithmus]] löst das Wortproblem für [[Kontextfreie Sprache|Kontextfreie Sprachen]]
- Wir studieren Algorithmen, die für eine gegebene [[Grammatik]] $G$ einen [[Automat|Automaten]] $A_G$ konstruieren, und untersuchen ihre Laufzeit. 

$A_G$ ist eine abstrakte Beschreibung eines Programms zur Lösung des Wortproblems.


Der Algorithmus mit $G$ als Eingabe und $A_G$ als Ausgabe ist eine abstrakte Beschreibung eines Programms für die automatische Synthese von [[Recognizer|Recognizern]] ([[lex & yacc]]).



# Zeit
#### DCFL
Das Wortproblem für [[DCFL|DCFLs]] ist in linearer Zeit lösbar.
