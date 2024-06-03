
# Definition
### Reflexivität
$\alpha \rightarrow{ }_G^0 \alpha$

**Reflexivität**: Die Beziehung ist reflexiv, das bedeutet, dass jedes Element zu sich selbst in Beziehung steht. In der Definition wird dies durch \($\alpha \rightarrow{_G^0} \alpha$\) ausgedrückt. Das bedeutet, dass es **keinen** Schritt gibt, um von \($\alpha$\) zu ($\alpha$) zu gelangen (also 0 Schritte).

### Transitivität
$\alpha \rightarrow_G^{n+1} \gamma: \Leftrightarrow \quad \exists \beta . \alpha \rightarrow_G^n \beta \rightarrow_G \gamma$

**Transitivität**: Die Beziehung ist transitiv. Wenn du von einem Zustand \($\alpha$\) zu einem Zustand \($\beta$\) in einer bestimmten Anzahl von Schritten \($n$\) gelangen kannst und von \($\beta$\) zu einem weiteren Zustand \($\gamma$\) in einem weiteren Schritt, dann kannst du auch direkt von \($\alpha$\) zu \($\gamma$) in \($n+1$\) Schritten gelangen. Das wird in der Definition durch die Regel ($\alpha \rightarrow{_G^{n+1}} \gamma: \Leftrightarrow \quad \exists \beta \cdot \alpha \rightarrow{_G^n} \beta \rightarrow{_G} \gamma$\) verdeutlicht.


### Reflexiv und Transitive Hülle
$\alpha \rightarrow_G^* \beta: \Leftrightarrow \quad \exists n . \alpha \rightarrow_G^n \beta$
$\alpha$ kann in 0 oder $n$ Schritten zu $\beta$
Man kann $\beta$ erzeugen in 0 oder mehr Schritten.

**Reflexive Transitive Hülle (($\rightarrow{_G^*}$))**: Dies bedeutet, dass es eine beliebige Anzahl von Schritten (einschließlich null Schritte) gibt, um von ($\alpha$) zu ($\beta$) zu gelangen. Mathematisch wird das als ($\alpha \rightarrow{_G^*} \beta: \Leftrightarrow \quad \exists n . \alpha \rightarrow{_G^n} \beta$) definiert.

### Transitive Hülle
$\alpha \rightarrow_G^{+} \beta: \Leftrightarrow \quad \exists n>0 . \alpha \rightarrow_G^n \beta$

**Transitive Hülle (\($\rightarrow{_G^+}$\))**: Hier gibt es eine positive Anzahl von Schritten, um von \($\alpha$\) zu \($\beta$\) zu gelangen. Anders als bei der reflexiven transitiven Hülle wird hier mindestens ein Schritt benötigt. In der Formel ausgedrückt: ($\alpha \rightarrow{_G^+} \beta: \Leftrightarrow \quad \exists n>0 . \alpha \rightarrow{_G^n} \beta$).


_____
# Beispiel
$\langle$ Expr $\rangle \rightarrow{ }_G^{11} a *(b+c)$ und so $\langle\mathrm{Expr}\rangle \rightarrow_G^* a *(b+c)$. 

Es gilt:
$L(G)=\left\{w \in \Sigma^* \mid S \rightarrow_G^* w\right\}$
	-> Erklärt: L(G) beschreibt die Sprache von $G$, die alle Wörter $w$ enthält, die in denen es in beliebig vielen Schritten eine Ableitung aus $S$ gibt.



### Beispiel:
Das Beispiel \($\langle\operatorname{Expr}\rangle \rightarrow{_G^{11}} a \ast (b+c)$) zeigt, dass es 11 Schritte benötigt, um von ($\langle\operatorname{Expr}\rangle$) zu $(a \ast (b+c)$\) zu gelangen. Und weil es eine Verbindung gibt, folgt daraus auch, dass \($\langle\mathrm{Expr}\rangle \rightarrow{_G^*} a \ast (b+c)$\), also eine reflexive transitive Verbindung existiert.


### Sprache (L(G)):
Die Menge \($L(G) = \left\{w \in \Sigma^* \mid S \rightarrow{_G^*} w\right\}$\) beschreibt die Sprache von ($G$), welche alle Wörter ($w$) umfasst, zu denen es eine Ableitung von ($S$) aus in beliebig vielen Schritten gibt.



_____
# Von Folien
$$\begin{aligned}
\alpha \rightarrow_G^0 \alpha & \\
\alpha \rightarrow_G^{n+1} \gamma & : \Leftrightarrow \quad \exists \beta . \alpha \rightarrow_G^n \beta \rightarrow_G \gamma \\
\alpha \rightarrow_G^* \beta & : \Leftrightarrow \quad \exists n . \alpha \rightarrow_G^n \beta \\
\alpha \rightarrow_G^{+} \beta & : \Leftrightarrow \quad \exists n>0 . \alpha \rightarrow_G^n \beta
\end{aligned}$$

Beispiel: $E \rightarrow_G^{11} a *(a+a) \text { und daher } E \rightarrow_G^* a *(a+a)$

