#theo/definition
ist NICHT [[semi-entscheidbar (s-e)]]
==Eine Menge ist nicht semi-entscheidbar **genau dann, wenn** die [[semi-charakteristische Funktion]] $\chi_A^{\prime}$ unberechenbar ist.==


# Spezifizierung
Mein Guess war, dass die untenstehende Funktion unentscheidbar ist. 
Und somit nicht-semi-entscheidbar. Jedoch stimmt das nicht (aus [zulip frage](https://zulip.in.tum.de/#narrow/stream/2196-THEO-SS24-Allgemein/topic/nicht.20semi-entscheidbar)):
	$\chi_A^{\prime}$ ist die Funktion aus Definition 5.42, die "[[semi-charakteristische Funktion]]". Die Funktion $x \mapsto\left\{\begin{array}{ll}\perp & \text { falls } x \in A \\ \perp & \text { falls } x \notin A\end{array}\right.$ ist einfach die überall undefinierte Funktion und hat nichts mit $A$ zu tun.


# Grafik
Roter Bereich ohne gelb ist nicht-semi-entscheidbar
![[entscheidbar#Übersicht entscheidbar]]



# von zulip
Naja, es bedeutet, dass es nicht eine der Sprachen ist, die semi-entscheidbar sind :) Die Intuition ist, dass man nach endlicher Zeit nicht feststellen kann, dass ein Wort in der Sprache enthalten ist. Das leichteste Beispiel ist das Komplement vom Halteproblem (allgemein, speziell, leeres Band). Man kann sich nie sicher sein, dass eine TM nicht hält.
Ein anderes wichtiges Beispiel ist das Terminierungsproblem $\mathcal{H}_{\Sigma^*}=\{w\mid\forall x:M_w[x]{\downarrow}\}$, 
also ob eine TM auf jeder Eingabe hält. Das Problem ist nicht semi-entscheidbar, und sein Komplement ist auch nicht semi-entscheidbar.

