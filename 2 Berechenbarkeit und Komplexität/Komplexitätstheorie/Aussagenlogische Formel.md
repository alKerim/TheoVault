# Syntax der Aussagenlogik
Formeln: $\quad F \rightarrow \neg F|(F \wedge F)|(F \vee F) \mid X$
Variablen: $X \rightarrow x|y| z \mid \ldots$

Bsp: $((\neg x \wedge y) \vee(x \wedge \neg z))$


# Semantik der Aussagenlogik
- Eine Belegung ist eine Funktion von Variablen auf $\{0,1\}$. Bsp: $\sigma=\{x \mapsto 0, y \mapsto 1, z \mapsto 0, \ldots\}$
- Belegungen werde mittels Wahrheitstabellen auf Formeln erweitert. Bsp: $\sigma((\neg x \wedge y) \vee(x \wedge \neg z))=1$
- Eine Formel $F$ ist [[erfüllbar]] gdw es eine Belegung $\sigma$ gibt mit $\sigma(F)=1$

