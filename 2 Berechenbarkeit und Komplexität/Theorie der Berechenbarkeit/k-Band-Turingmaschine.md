Eine beliebte Modellvariante der [[Turingmaschine - TM|TM]] ist die $k$-Band-Turingmaschine:
![[Screenshot 2024-06-13 at 15.38.45.png]]
Die $k$ Köpfe sind völlig unabhängig voneinander:
$$\begin{equation*}
\delta: Q \times \Gamma^k \rightarrow Q \times \Gamma^k \times\{L, R, N\}^k
\end{equation*}$$



# Simuliert durch 1-Band-TM
Jede $k$-Band-Turingmaschine kann effektiv durch eine 1-Band-TM simuliert werden.

![[Screenshot 2024-06-17 at 14.19.55.png|500]]
- $\Gamma^{\prime}:=(\Gamma \times\{\star, \square\})^k$
- $M^{\prime}$ simuliert einen $M$-Schritt durch mehrere Schritte: $M^{\prime}$
- startet mit Kopf links von allen $\star$.
- geht nach rechts bis alle $\star$ überschritten sind, und merkt sich dabei (in $Q^{\prime}$ ) die Zeichen über jedem $\star$.
- hat jetzt alle Information, um $\delta_M$ anzuwenden.
- geht nach links über alle $\star$ hinweg und führt dabei $\delta_M$ aus.


Beobachtung:
#theo/zeit 
- $n$ Schritte von $M$ lassen sich durch $O\left(n^2\right)$ Schritte von $M^{\prime}$ simulieren.
- Denn nach $n$ Schritten von $M$ trennen $\leq 2 n$ Felder linkesten und rechtesten Kopf. Obige Simulation eines $M$-Schritts braucht daher $O(n)$ $M^{\prime}$-Schritte. Simulation von $n$ Schritten: $O\left(n^2\right)$ Schritte.


