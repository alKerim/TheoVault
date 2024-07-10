

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
TODO

### $L \subseteq L(G)$
TODO


