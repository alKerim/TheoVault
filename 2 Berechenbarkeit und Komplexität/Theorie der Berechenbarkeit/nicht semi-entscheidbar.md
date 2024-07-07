#theo/definition
ist NICHT [[semi-entscheidbar (s-e)]]

# Grafik
Roter Bereich ohne gelb ist nicht Semi-Entscheidbar
![[entscheidbar#Übersicht entscheidbar]]



# von zulip
Naja, es bedeutet, dass es nicht eine der Sprachen ist, die semi-entscheidbar sind :) Die Intuition ist, dass man nach endlicher Zeit nicht feststellen kann, dass ein Wort in der Sprache enthalten ist. Das leichteste Beispiel ist das Komplement vom Halteproblem (allgemein, speziell, leeres Band). Man kann sich nie sicher sein, dass eine TM nicht hält.
Ein anderes wichtiges Beispiel ist das Terminierungsproblem $\mathcal{H}_{\Sigma^*}=\{w\mid\forall x:M_w[x]{\downarrow}\}$, 
also ob eine TM auf jeder Eingabe hält. Das Problem ist nicht semi-entscheidbar, und sein Komplement ist auch nicht semi-entscheidbar.

