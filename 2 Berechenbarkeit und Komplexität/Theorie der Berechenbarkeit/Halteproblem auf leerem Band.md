$H_0:=\left\{w \in\{0,1\}^* \mid M_w[\epsilon] \downarrow\right\}$

# Unentscheidbarkeit
Das [[Halteproblem]] auf leerem Band, $H_0$, ist [[unentscheidbar]].
### Beweis
Wir zeigen $K \leq H_0$ mit einer Funktion $f:\{0,1\}^* \rightarrow\{0,1\}^*$ $f(w)$ ist die Kodierung folgender TM:
![[Screenshot 2024-06-20 at 15.32.07.png|350]]

Überschreibe die Eingabe mit $w$; führe $M_w$ aus.

![[Screenshot 2024-06-20 at 15.34.55.png|400]]



Dh $f$ berechnet aus $w$ die Kodierung $w_1$ einer [[Turingmaschine - TM|TM]], die $w$ schreibt, und gibt die Kodierung von " $w_1 ; w$ " zurück.
Damit ist $f$ [[total]] und [[berechenbar]].
Es gilt:
#theo/wichtig #theo/reduktion 
$$\begin{equation*}
w \in K \Leftrightarrow M_w[w] \downarrow \Leftrightarrow M_{f(w)}[\epsilon] \downarrow \Leftrightarrow f(w) \in H_0
\end{equation*}$$



	