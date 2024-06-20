Gegeben: Ein Wort $w \in\{0,1\}^*$.
Problem: Hält $M_w$ bei Eingabe $w$ ?
Als Menge:
$$\begin{equation*}
K:=\left\{w \in\{0,1\}^* \mid M_w[w] \downarrow\right\}
\end{equation*}$$


# Nicht entscheidbar
Das spezielle Halteproblem ist [[nicht entscheidbar]].

### Beweis
Angenommen, $K$ sei entscheidbar, dh $\chi_K$ ist berechenbar. Dann ist auch folgende Funktion $f$ berechenbar:
$$\begin{equation*}
f(w):=\left\{\begin{array}{ll}
0 & \text { falls } \chi_K(w)=0 \\
\perp & \text { falls } \chi_K(w)=1
\end{array}\right.
\end{equation*}$$
$\chi_K$ =  [[charakteristische Funktion]]


Denn berechnet eine TM $M$ die Funktion $\chi_K$, so berechnet die folgende TM $M^{\prime}$ die Funktion $f$ :
![[Screenshot 2024-06-20 at 15.01.39.png|400]]
Dann gibt es ein $w^{\prime}$ mit $M_{w^{\prime}}=M^{\prime}$.

$$\begin{equation*}
\begin{array}{l}
f\left(w^{\prime}\right)=\perp \quad \Leftrightarrow \quad \chi_K\left(w^{\prime}\right)=1 \quad \text { (Def. von } f \text { ) } \\
\Leftrightarrow \quad w^{\prime} \in K \quad \text { (Def. von } \chi_K \text { ) } \\
\Leftrightarrow \quad M_{w^{\prime}}\left[w^{\prime}\right] \downarrow \quad \text { (Def. von } K \text { ) } \\
\Leftrightarrow \quad M^{\prime}\left[w^{\prime}\right] \downarrow \quad\left(M_{w^{\prime}}=M^{\prime}\right) \\
\Leftrightarrow \quad f\left(w^{\prime}\right) \neq \perp \quad\left(M^{\prime} \text { berechnet } f\right) \\
\end{array}
\end{equation*}$$

Wir erhalten einen Widerspruch: 
$f\left(w^{\prime}\right)=\perp \Leftrightarrow f\left(w^{\prime}\right) \neq \perp$. Die Annahme, $K$ sei [[entscheidbar]], ist damit falsch.



