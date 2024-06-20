Eine Turingmaschine (TM) ist ein 7-Tupel $M=\left(Q, \Sigma, \Gamma, \delta, q_0, \square, F\right)$ so dass
- $Q$ ist eine endliche Menge von Zuständen.
- $\Sigma$ ist eine endliche Menge, das Eingabealphabet.
- $\Gamma$ ist eine endliche Menge, das Bandalphabet, mit $\Sigma \subset \Gamma$ (nicht $\subseteq$ weil es in $\Gamma$ Symbole gibt die nicht in $\Sigma$ sind)
- $\delta: Q \times \Gamma \rightarrow Q \times \Gamma \times\{L, R, N\}$ ist die Übergangsfunktion. $\delta$ darf partiell sein.
- $q_0 \in Q$ ist der Startzustand.
- $\square \in \Gamma \backslash \Sigma$ ist das Leerzeichen.
- $F \subseteq Q$ ist die Menge der akzeptierenden oder Endzustände.

- Annahme(==wichtig==): $\delta(q, a)$ is nicht definiert für alle $q \in F$ und $a \in \Gamma$. 
	Endzustände haben keine ausgehenden Kanten #theo/wichtig 
- Keine **totale** Übergangsfunktion nötig, ABER deterministische Übergänge!!! #theo/wichtig 
- Eine [[Nichtdeterminismus|nichtdeterministische]] Turingmaschine hat eine Übergangsfunktion $\delta: Q \times \Gamma \rightarrow \mathcal{P}(Q \times \Gamma \times\{L, R, N\})$.

____
![[Turingmaschine - TM#^bb8ab1]]
![[Turingmaschine - TM#^f4aa6e]]
_____


![[Screenshot 2024-06-13 at 14.52.58.png|400]]
![[Screenshot 2024-06-15 at 15.28.20.png]]


# Konfigurationen
Eine Konfiguration einer Turingmaschine ist ein Tripel
$$\begin{equation*}
(\alpha, q, \beta) \in \Gamma^* \times Q \times \Gamma^* \text {. }
\end{equation*}$$


Dies modelliert
- Bandinhalt: ... $\square \alpha \beta \square \ldots$
- Zustand: $q$
- Kopf auf dem ersten Zeichen von $\beta \square$

#### Startkonfiguration
Die Startkonfiguration der Turingmaschine bei Eingabe $w \in \Sigma^*$ ist $\left(\epsilon, q_0, w\right)$.

==WICHTIG==: Kopf liegt auf erstem Zeichen des Input Wortes. #theo/wichtig 
Also zB bei Sprache $a^nb^n$ liegt der Zeiger auf dem ersten $a$ des Wortes

#### Endkonfiguration
###### Output Aufgabe
Also eine Aufgabe wie
Konstruieren Sie eine Turingmaschine $T=\left(Q, \Sigma, \Gamma, q_0, \square, \delta, F\right)$, mit $\Sigma=\{\mid\}$, die eine eingegebene Strichzahl verdoppelt.
--->> Der Kopf muss am Anfang des Wortes stehen (auf dem 1. Zeichen) #theo/wichtig 
###### Bool Aufgabe
Konstruiere eine TM die, die folgende Sprache akzeptiert
zB. $a^nb^nc^n$ 
Dann muss am Ende nur in einen Endzustand gegangen werden, egal was in dem Feld auf das der Kopf zeigt steht.

#### intuitiv
Intuitiv bedeutet $\quad \delta(q, a)=\left(q^{\prime}, b, D\right)$ :
- Wenn sich $M$ im Zustand $q$ befindet,
- und auf dem Band $a$ liest,
- so geht $M$ im nächsten Schritt in den Zustand $q^{\prime}$ über,
- überschreibt $a$ mit $b$,
- und bewegt danach den Schreib-/Lesekopf nach rechts (falls $D=R$ ), nach links (falls $D=L$ ), oder nicht (falls $D=N$ ).



# TM akzeptiert
Eine Turingmaschine $M$ akzeptiert die Sprache ^bb8ab1
$$\begin{equation*}
L(M)=\left\{w \in \Sigma^* \mid \exists q \in F, \alpha, \beta \in \Gamma^* .\left(\epsilon, q_0, w\right) \rightarrow_M^*(\alpha, q, \beta)\right\}
\end{equation*}$$

^f4aa6e

![[Turing-berechenbar]]



# Hintereinanderschaltung von TMs
[[Hintereinanderschaltung von TMs]]

