#theo/beweis 

### $L\left(G^{\prime}\right) \subseteq L(G)$ (Grammatik in Grammatik)
#### Beispiele
Sei $G$ eine beliebige Grammatik, und $G^{\prime}$ eine Grammatik, die durch das Entfernen von einer beliebigen Produktion aus $G$ entsteht. Beweisen oder widerlegen Sie $L\left(G^{\prime}\right) \subseteq L(G)$

Lösung:
	Die Aussage ist wahr: Sei $w \in L\left(G^{\prime}\right)$ beliebig, und $S$ das Startsymbol von $G$. Nach Definition von $L\left(G^{\prime}\right)$ gilt also $S \rightarrow_{G^{\prime}}^* w$. Da wir für $G^{\prime}$ aber nur eine Produktion entfernt haben, gilt $S \rightarrow_G^* w$ ebenfalls, und somit $w \in L(G)$.
	1. Wähle $w$ von links
	2. Zeige Ableitung von $w$ mit linker Grammatik $G'$
	3. Zeige es gibt auch Ableitung von $w$ mit rechter $G$
	4. Konkludiere, deshalb $w \in L(G)$



### $L(G) \subseteq L$
#theo/cheatsheet 
##### Beispiel: Repetitorium 23 (21.9.23)
Aufgabe 12. Sei $G=(\{S\},\{a, b\}, P, S)$ die Grammatik mit den Produktionen
$S \rightarrow a S a|b S b| a \mid b$ und $L=\left\{w \in\{a, b\}^*\left|w=w^R,\right| w \mid\right.$ ungerade $\}$.
(a) Zeigen Sie $L(G) \subseteq L$ mittels struktureller Induktion.
Lösung:
	Induktionsanfang: Es gilt $a \in L$ und $b \in L$.
	Induktionshypothese: $w \in L$.
	Induktionsschritt: $|a w a|$ ist ungerade, weil $|w|$ per IH ungerade ist. 
	Außerdem gilt $(a w a)^R=a w^R a \stackrel{I H}{=}$ awa. Es folgt $a w a \in L$. Der Fall $b w b$ funktioniert analog.


### $L \subseteq L(G)$
#theo/cheatsheet  
##### Beispiel: Repetitorium 23 (21.9.23)
Aufgabe 12. Sei $G=(\{S\},\{a, b\}, P, S)$ die Grammatik mit den Produktionen
$S \rightarrow a S a|b S b| a \mid b$ und $L=\left\{w \in\{a, b\}^*\left|w=w^R,\right| w \mid\right.$ ungerade $\}$.
(b) Zeigen Sie $L \subseteq L(G)$ mittels Induktion über die Wortlänge.
Lösung:
	Wir zeigen $w \in L \Rightarrow w \in L(G)$ per Induktion über $|w|$.
	**Induktionsanfang**: $\varepsilon \notin L$, also ist $\varepsilon \in L \Rightarrow \varepsilon \in L(G)$ wahr.
	**Induktionshypothese**: Für alle $u \in\{a, b\}^*$ mit $|u|<|w|$ gilt $|u| \in L \Rightarrow$ $u \in L(G)$.
	**Induktionsschritt**: 
	Sei $w \in L$. Falls $|w|=1$, so gilt $w \in\{a, b\}$, also $w \in L(G)$. 
		Ansonsten gilt $|w| \geq 3$ und $w=w^R$, d.h. $w$ ist von der Form $x w^{\prime} x$ mit $x \in\{a, b\}$ und $w^{\prime}=w^{\prime R}$. 
		Da $|w|$ ungerade ist, ist $\left|w^{\prime}\right|$ auch ungerade. 
		Also $w^{\prime} \in L$, und per IH folgt $w^{\prime} \in L(G)$.
		 Somit gilt $S \rightarrow w^{\prime}$, also auch $S \rightarrow x S x \rightarrow^* x w^{\prime} x=w$, 
	d.h. $w \in L(G)$.




