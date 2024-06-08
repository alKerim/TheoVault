Eine Sprache ist **regulär** gdw sie von einem [[DFA - Deterministische endliche Automaten|DFA]] akzeptiert wird.
Eine Sprache ist **regulär** gdw sie von einem [[NFA - Nichtdeterministische endliche Automaten|NFA]] akzeptiert wird.
	Bei komplizierteren Sprachen muss aber auch klar sein, dass dieser NFA tatsächlich die entsprechende Sprache erzeugt - unter Umständen muss man das dann noch beweisen/begründen. Bei einfacheren Sprachen ist das oft direkt klar.
Eine Sprache ist **regulär** gdw sie von einem [[RE - Reguläre Ausdrücke|Reguläre Ausdruck]] erzeugt wird.
Eine Sprache ist **regulär** gdw sie von einer [[Rechtslineare Grammatiken|Rechtslineare Grammatik]] erzeugt wird.
Eine Sprache ist **regulär** gdw sie endlich viele [[Residualsprache|Residualsprachen]] hat.
Eine reguläre Sprache ist unter folgender [[Abschlusseigenschaften regulärer Sprachen|Abschlusseigenschaften]] **regulär**.


Jede [[endliche Sprache]] ist **regulär**.
	Aber nicht jede reguläre Sprache ist endlich. 
	-> Beispiel $L(a^*)$ ^0d53a2




_____
# nicht-regulär
Zu zeigen durch:
- [[Pumping Lemma]] (geht nicht immer, wegen Hinreichend)
- Zeigen, dass $L$ unendlich viele [[Residualsprache|Residualsprachen]] hat.... [[theo-folien-handout.pdf#page=131|Beispiel hier]]
- reguläre Sprachen sind über dem Komplement abgeschlossen. Wenn $\bar{L}$ regulär wäre, wäre folglich auch $\bar{\bar{L}}=L$ regulär. Wir wissen allerdings, dass zB L nicht regulär, dann ist $\bar{L}$ auch nicht regulär.



____

# weder regulär, noch nicht-regulär (disproved)
TODO check dis out: 
![[Screenshot 2024-05-17 at 14.28.37.png]]
Lösung: nur a) und b) stimmen

