![[nützlich (theo)#^a2c85a]]

![[nützlich (theo)#^39adb8]]
![[erzeugend (theo)#^5ac3ef]]
![[erreichbar (theo)#^516aa3]]

____

![[nützlich (theo)#Relation]]

____
# Elimination
Eliminiert man aus einer Grammatik $G$
(1) alle nicht erzeugenden Symbole, mit Resultat $G_1$, und
(2) aus $G_1$ alle unerreichbaren Symbole, mit Resultat $G_2$, dann enthält $G_2$ nur noch nützliche Symbole und $L\left(G_2\right)=L(G)$.
#### Beweis
Wir zeigen zuerst $L\left(G_2\right)=L(G)$.
Da $P_2 \subseteq P$ gilt $L\left(G_2\right) \subseteq L(G)$. ($P$ und $P_2$ sind die Produktionen von $L(G)$ und $L(G_2)$ )
Umgekehrt, sei $w \in L(G)$, dh $S \rightarrow_G^* w$.
Jedes Symbol in dieser Ableitung ist erreichbar und erzeugend.
Also gilt auch $S \rightarrow_{G_2}^* w$, dh $w \in L\left(G_2\right)$.

Weiter:
$\left[G_1\right.$ : erzeugend in $G, G_2:$ erreichbar in $\left.G_1\right]$
Wir zeigen: Alle $X \in V_2 \cup \Sigma_2$ sind nützlich in $G_2$, dh
$$\begin{equation*}
S \quad \rightarrow_{G_2}^* \quad \ldots X \ldots \quad \rightarrow_{G_2}^* \quad \ldots \in \Sigma_2^*
\end{equation*}$$
$X$ muss in $G_1$ erreichbar sein, dh $S \rightarrow_{G_1}^* \alpha X \beta$.
Da alle Symbole in der Ableitung erreichbar sind: $S \rightarrow_{G_2}^* \alpha X \beta$.
Alle Symbole in $\alpha X \beta$ müssen in $G$ erzeugend sein:
$$\begin{equation*}
\forall Y \in \alpha X \beta . \exists u \in \Sigma^* . Y \rightarrow_G^* u
\end{equation*}$$

Da alle Symbole in den Ableitungen $Y \rightarrow_G^* u$ erzeugend sind:
$$\begin{equation*}
\forall Y \in \alpha X \beta . \exists u \in \Sigma_1^* . Y \rightarrow_{G_1}^* u
\end{equation*}$$

Also gibt es $w \in \Sigma_1^*$ mit $\alpha X \beta \rightarrow_{G_1}^* w$.
Die Ableitung $\alpha X \beta \rightarrow_{G_1}^* w$ enthält nur Symbole, die in $G_1$ erreichbar sind. Daher auch $\alpha X \beta \rightarrow_{G_2}^* w$.
$$\begin{equation*}
S \rightarrow_{G_2}^* \alpha X \beta \rightarrow_{G_2}^* w
\end{equation*}$$


# Elimination Algorithmus 
![[IMG_4477.jpg]]
