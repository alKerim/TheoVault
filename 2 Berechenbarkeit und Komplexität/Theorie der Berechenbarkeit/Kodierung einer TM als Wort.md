Kodierung einer [[Turingmaschine - TM|TM]] als Wort über $\Sigma=\{0,1\}$, exemplarisch:
- Sei $\Gamma=\left\{a_0, \ldots, a_k\right\}$ und $Q=\left\{q_0, \ldots, q_n\right\}$.
- $\delta\left(q_i, a_j\right)=\left(q_{i^{\prime}}, a_{j^{\prime}}, d\right)$ wird kodiert als
$$\begin{equation*}
\# b i n(i) \# b i n(j) \# b i n\left(i^{\prime}\right) \# b i n\left(j^{\prime}\right) \# b i n(m)
\end{equation*}$$
wobei bin: $\mathbb{N} \rightarrow\{0,1\}^*$ die Binärkodierung einer Zahl ist und $m=0 / 1 / 2$ falls $d=L / R / N$.
- Kodierung von $\delta$ : Konkatenation der Kodierungen aller $\delta(.,)=.(., .,$.$)$ , in beliebiger Reihenfolge.
- Kodierung von $\{0,1, \#\}^*$ in $\{0,1\}^*$ :
$$\begin{equation*}
\begin{array}{rll}
0 & \mapsto & 00 \\
1 & \mapsto & 01 \\
\# & \mapsto & 11
\end{array}
\end{equation*}$$
# Nicht jedes Wort TM
Nicht jedes Wort über $\{0,1\}^*$ kodiert eine TM.
Sei $\hat{M}$ eine beliebige feste TM.



# TM $M_w$ erstellt durch $w$
Die zu einem Wort $w \in\{0,1\}^*$ gehörige TM $M_w$ ist
$$\begin{equation*}
M_w:=\left\{\begin{array}{ll}
M & \text { falls } w \text { Kodierung von } M \text { ist } \\
\hat{M} & \text { sonst }
\end{array}\right.
\end{equation*}$$
Die Kodierung von syntaktischen Objekten (Programmen, Formeln, etc) als Zahlen nennt man [[Gödelisierung]] und die Zahlen Gödelnummern.

### $M_w\downarrow$ 
$M[w]$ ist Abk. für „,Maschine $M$ mit Eingabe $w^{\text {“ }}$ 
$M[w] \downarrow$ bedeutet, dass $M[w]$ terminiert/hält.

### $M_w\uparrow$ 
$M[w] \uparrow$ bedeutet, dass $M[w]$ NICHT terminiert/hält.


### $M_w\downarrow$  vs. $M_w\uparrow$ 
$$g(\omega)=\left\{\begin{array}{llll}
0 & \text { gdw }  & M_\omega[\omega] \uparrow & gdw. f(w)=0 \\
1 & \text { gdw } & M_\omega[\omega] \downarrow & gdw. f(w)= \perp
\end{array}\right.$$
## aus tweedback
Wieso sagen wir Mw[w] terminiert nicht, gdw f(w)=0, was genau macht denn f(w) eigentlich ?
Weil wir f so definiert haben. f(w_i) = 0 gdw. M_{w_i}(w_i) nicht terminiert und f(w_i) ist undefiniert gdw. M_{w_i}(w_i) terminiert.
Aber wie wissen wir dass M_{w_i)(w_i) nicht terminiert, wenn es nie terminiert
Das ist erstmal unerheblich, da wir die Funktion genau so definieren.

wtf

Was Du als "wissen" bezeichnest bezieht sich eigentlich schon auf die Intuition von Berechenbarkeit. Du argumentierst, dass wir nicht wissen können, ob die Maschine terminiert, weil wir es ja nicht berechnen können. Fakt ist aber, dass die Maschine entweder terminiert oder nicht.

 0 Likes

Reply from  I07atTUM

 a few seconds ago

This reply is approved and visible to all participants.

Die Funktion f nimmt als den entsprechenden Wert an.

