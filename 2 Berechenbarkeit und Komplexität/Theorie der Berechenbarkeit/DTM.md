Deterministische Mehrband-[[Turingmaschine - TM|TM]]

Zu jeder nichtdeterministischen TM $N$ gibt es eine deterministische $TM$ genannt $M$ mit $L(N)=L(M)$.
	Beweis:
	$M$ durchsucht den Baum der Berechnungen von $N$ in Breitensuche, beginnend mit der Startkonfiguration $\left(\epsilon, q_0, w\right)$, eine Ebene nach der anderen.
	Gibt es in dem Baum (auf Ebene $n$ ) eine Konfigurationen mit Endzustand, so wird diese (nach Zeit $O\left(c^n\right)$ ) gefunden.

