#theo/probleme 
Sei $D$ ein DFA, NFA, RE, rechtslineare Grammatik ....

Leerheitsproblem: Gegeben $D$, gilt $L(D)=\emptyset$ ?


# Entscheidbarkeit
Für [[NFA - Nichtdeterministische endliche Automaten|NFAs]] und [[DFA - Deterministische endliche Automaten|DFAs]] [[entscheidbar]] 
(in Zeit $O\left(|Q|^2|\Sigma|\right)$ bzw $O(|Q||\Sigma|)$ ). #theo/zeit 

### Beweis / Vorgehen
#theo/algorithmus 
$L(M)=\emptyset$ gdw kein Endzustand von $q_0$ erreichbar ist.
Dies ist eine einfache Suche in einem Graphen, die jede Kante maximal ein $\mathrm{Mal}$ benutzen muss.
Ein NFA hat $\leq|Q|^2|\Sigma|$ Kanten, ein DFA hat $\leq|Q||\Sigma|$ Kanten.
Ist $\Sigma$ fix, z.B. ASCII, so wird daraus $O\left(|Q|^2\right)$ bzw $O(|Q|)$.

