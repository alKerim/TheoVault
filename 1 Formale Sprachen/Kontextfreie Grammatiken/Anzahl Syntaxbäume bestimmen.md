Für eine Grammatik $G$, die...
# ...[[kontextfrei]], in [[Chomsky-Normalform|CNF]]
1. Terminalproduktionen ($X \rightarrow b$)
	Wenn man in einem Syntaxbaum von $w$ alle Produktionen der Form $X \rightarrow a$ weglässt, erhält man einen vollen Binärbaum mit $n+1$ Blättern, in dem jeder Knoten mit einem Nichtterminal beschriftet ist. 
2. Nichtterminalproduktionen ($X \rightarrow YZ$)
	Da $G$ in CNF ist, erhalten wir aus $S$ ein **Wort der Länge** $n+1$ aus Nichtterminalen in genau $n$ Schritten, und **jeder Schritt fügt zwei neue Knoten zum Binärbaum hinzu**. 
	Insgesamt hat der Baum also $2 n+1$ Knoten. 
	Die Wurzel muss mit $S$ beschriftet sein, für die anderen $2 n$ Knoten gibt es jeweils höchstens $k$ Möglichkeiten, jeder Binärbaum hat also höchstens $k^{2 n}$ Möglichkeiten für Beschriftungen. 
	Laut Hinweis gibt es insgesamt $C_n$ Binärbäume mit $n+1$ Blättern; insgesamt hat $w$ also höchstens $k^{2 n} C_n$ Syntaxbäume. Diese Obergrenze wird durch die Grammatik in CNF, die alle möglichen Produktionen enthält, erreicht.
Kurzfassung