# Algorithmus
### Schritt 1: Gleichungssystem aufstellen (geht auch für $\epsilon$-NFAs)
Für einen NFA $N=\left(Q, \Sigma, \delta, q_0, F\right)$
1. Für jede Transition von $\delta(q_1,w)=q_2$ mit $q_1,q_2 \in Q$ und $w \in \Sigma \cup \{\epsilon\}$ folgendes hinzufügen:
	1. $X_{1}\equiv wX_2$ 
2. Für alle $q_i \in F$ füge folgende Gleichung hinzu:
	1. $X_{i}\equiv \epsilon$ 

### Schritt 2: Gleichungssystem lösen
Am Ende des Auflösens muss links der Gleichung $X_0$ der ursprüngliche Startzustand stehen.
- Also $X_{0}\equiv \ldots$ 
- Deswegen andere $X_i$ immer in $X_0$ einsetzen, nie $X_0$ woanders einsetzen beim auflösen

Siehe unten bei Beispiel oder VL-Folien slide 73, oder [Lösung HA3.3a), Schritte 1-7](https://teaching.model.in.tum.de/2024ss/theo/ex/ha03-solution.pdf?key=nSFcLMvc)

#### Schritt 3: Ardens Lemma anwenden
1. Siehe Defnition von [[Ardens Lemma]].
2. Beachte Fall falls $\epsilon \in \alpha$, dann NICHT anwenden. ([[Ardens Lemma#wichtig a*|Mehr dazu]])
3. Anwenden siehe anhand Beispiel unten oder [Lösung HA3.3a), Schritt (8)](https://teaching.model.in.tum.de/2024ss/theo/ex/ha03-solution.pdf?key=nSFcLMvc)


___
# Anhand Beispiel
#### Schritt 1: NFA als Gleichungssystem darstellen
![[Screenshot 2024-07-05 at 12.53.43.png|400]]
#### Schritt 2: Gleichungssystem lösen:
[[theo-folien-handout.pdf#page=73]]


#### Schritt 2.x: Eventually Ardens Lemma anwenden
[[Ardens Lemma]]

![[Screenshot 2024-07-05 at 13.05.28.png|500]]

