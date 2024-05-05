
# Frage 4
$|A B \cup A C| \geq|A(B \cap C)|$
Wahr oder Falsch ?
### Lösung:
[[Beweisen#$A subseteq B$|Beweisart $A \subseteq B$]]
$A B \cup A C=A(B \cup C) \supseteq A(B \cup C)$, da $B \cup C \supseteq B \cap C$

___

# Frage 5
$A \subseteq B \Leftrightarrow A^2 \subseteq B^2$
Wahr oder Falsch ?
### Lösung:
[[Beweisen#Angeben eines Gegenbeispiels|Gegenbeispiel]]: $A:=\{a\}, B:=\{\varepsilon, a a\}$. Es gilt $A^2 \subseteq B^2$ aber nicht $A \subseteq B$.
___

# Frage 6
$\left(A^2\right)^* \subseteq\left(A^*\right)^2$
Wahr oder Falsch ?
### Lösung:
$\left(A^2\right)^*=\bigcup_{i \in \mathbb{N}}\left(A^2\right)^i=\bigcup_{i \in \mathbb{N}} A^{2 i} \subseteq A^*=A^* A^*$

___
# Frage 7
Sei $G$ eine beliebige Grammatik über $\Sigma$, mit $L(G) \neq \emptyset$ und $L(G) \neq \Sigma^*$. 
Welche der folgenden Aussagen ist FALSCH? 
Bitte beachten Sie, dass die folgenden Aussagen für alle $G$ gelten müssen, und (abhängig von der Aussage) für ein $G^{\prime}$ oder für alle $G^{\prime}$.

Wählen Sie eine Antwort:
a. Es gibt eine Grammatik $G^{\prime}$, die durch das Löschen einer Produktionen aus $G$ entsteht, mit $L\left(G^{\prime}\right) \neq L(G)$.
b. Es gibt eine Grammatik $G^{\prime}$, die durch das Hinzufügen einer Produktionen zu $G$ entsteht, mit $L\left(G^{\prime}\right) \neq L(G)$.
c. Für eine beliebige Grammatik $G^{\prime}$, die durch das Entfernen mehrerer Produktionen aus $G$ entsteht, gilt $L\left(G^{\prime}\right) \subseteq L(G)$.
d. Für eine beliebige Grammatik $G^{\prime}$, die durch das Hinzufügen einer Produktionen zu $G$ entsteht, gilt $L\left(G^{\prime}\right) \supseteq L(G)$. 

### Lösung:
- a. FALSCH. zB: Angenommen $G$ ist $S \rightarrow A \mid B$ und $A \rightarrow a$ und $B \rightarrow a$.
  Egal welche Produktion man löscht, es gilt trotzdem $L(G')=\{a\}=L(G)$ 
- b. Wahr. Wie in a. aber andersherum
- c. Wahr:
  Sei $w \in L\left(G^{\prime}\right)$ beliebig, und $S$ das Startsymbol von $G$. Nach Definition von $L\left(G^{\prime}\right)$ gilt also $S \rightarrow_{G^{\prime}}^* w$. Da wir für $G^{\prime}$ aber nur eine Produktion entfernt haben, gilt $S \rightarrow_G^* w$ ebenfalls, und somit $w \in L(G)$.
  In meinen Worten zum Verständnis: Also im Prinzip wenn ein Wort $w \in L(G')$ dann auch $w \in L(G)$, weil nur eine Produktion entfernt wurde.
  - d. Wenn $G^{\prime}$ durch das Hinzufügen einer Produktion zu $G$ entsteht, dann ergibt sich $G$ durch das Entfernen einer Produktion aus $G^{\prime}$. Damit können wir das auf die aus der c)-Aufgabe bekannte Aussage zurückführen.


___

# Frage 8
### Aufgabenstellung:
Sei $G$ eine beliebige kontextfreie Grammatik über $\Sigma$ und $G^{\prime}$ eine Grammatik, die dadurch entsteht, dass man ein beliebiges Zeichen $\alpha$ (Terminal oder Nichtterminal) der rechten Seite einer Produktion von $G$ löscht (und $G$ ansonsten beibehält). Welche der folgenden Aussagen ist wahr? Wählen Sie eine Antwort: 
- a. Wenn $L(G)$ [[Sprache#Endlich|endlich]] ist und $\alpha$ ein Terminalzeichen, dann ist $L\left(G^{\prime}\right)$ auch endlich. 
- b. Wenn $L(G)$ endlich ist und $\alpha$ ein Nichtterminalzeichen, dann ist $L\left(G^{\prime}\right)$ auch endlich. 
- c. Wenn $L(G)$ [[Sprache#Unendlich|unendlich]] ist und $\alpha$ ein Terminalzeichen, dann ist $L\left(G^{\prime}\right)$ auch unendlich. 
- d. Wenn $L(G)$ unendlich ist und $\alpha$ ein Nichtterminalzeichen, dann ist $L\left(G^{\prime}\right)$ auch unendlich.

### Lösung:

Um diese Aufgabe zu lösen, müssen wir verstehen, wie das Entfernen eines Zeichens aus einer Grammatik die von dieser Grammatik erzeugte Sprache beeinflusst. Beginnen wir mit einigen grundlegenden Überlegungen zu kontextfreien Grammatiken und den Auswirkungen der Entfernung eines Symbols aus der rechten Seite einer Produktion.

1. **Was ist eine kontextfreie Grammatik?** Eine kontextfreie Grammatik ist eine Menge von Regeln, die beschreiben, wie Zeichenfolgen in einer Sprache gebildet werden. Diese Regeln bestehen aus Produktionen, die definieren, wie Nichtterminalsymbole durch eine Kombination von Terminal- und Nichtterminalsymbolen ersetzt werden können.

2. **Einfluss des Entfernens eines Symbols auf die Sprache:** Das Entfernen eines Symbols aus einer Produktion einer Grammatik könnte dazu führen, dass weniger oder einfachere Zeichenfolgen erzeugt werden können. 

Nun zu den spezifischen Aussagen und Überlegungen:
- **Aussage a**: Wenn $\alpha$ ein Terminalzeichen ist und aus einer Produktion entfernt wird, reduziert dies die spezifischen Wörter, die produziert werden können, um das Zeichen $\alpha$. Wenn $L(G)$ endlich ist, bleibt $L(G^\prime)$ auch endlich, da das Entfernen von $\alpha$ nicht dazu führt, dass plötzlich unendlich viele neue Wörter generiert werden können.

- **Aussage b**: Das Entfernen eines Nichtterminalzeichens könnte die Struktur der Produktionen erheblich beeinflussen, insbesondere wenn das Nichtterminal in rekursiven Produktionen verwendet wird, die zur Unendlichkeit von $L(G)$ beitragen. Wenn $L(G)$ jedoch endlich ist, bedeutet dies, dass es keine solche rekursive Produktion gibt, die unendlich viele Wörter erzeugt. Daher sollte $L(G^\prime)$ auch endlich bleiben.

- **Aussage c und d**: Wenn $L(G)$ unendlich ist, ist dies oft durch die Anwesenheit von rekursiven Produktionen bedingt. Das Entfernen eines Terminalzeichens aus einer Produktion entfernt einfach bestimmte spezifische Wörter oder macht einige Wörter kürzer, eliminiert jedoch nicht die Möglichkeit, unendlich viele Wörter zu erzeugen, solange die rekursiven Muster der Produktionen nicht beeinträchtigt sind. Ebenso könnte das Entfernen eines Nichtterminals, abhängig von seiner Rolle in rekursiven Mustern, die Unendlichkeit beeinflussen, aber das ist spezifisch und kann nicht generell gesagt werden, ohne die spezifische Struktur von $G$ zu kennen.

### Musterlösung:
Lösungsskizze. 
- (a) Sei $w \in L\left(G^{\prime}\right)$, also $S \rightarrow_{G^{\prime}}^* w$. (für Notation links sie [[Reflexiv transitive Hülle]]) 
  Wenn man die gleichen Produktionen in $G$ ausführt, erhält man ein Wort $w^{\prime}$. 
  Dieses enthält alle Zeichen aus $w$, möglicherweise mit Kopien von $c$ dazwischen. 
  Da $c$ ein Terminal ist, gilt $w^{\prime} \in L(G)$. Außerdem erhalten wir $\left|w^{\prime}\right| \geq|w|$. 
	  Wenn $L\left(G^{\prime}\right)$ unendlich wäre, gäbe es beliebig lange Wörter $w$ in $L\left(G^{\prime}\right)$, und somit beliebig lange Wörter $w^{\prime} \in L(G)$. 
	  Aber dann ist $L(G)$ auch unendlich. Da $L(G)$ endlich ist, muss $L\left(G^{\prime}\right)$ es auch sein. 
- (b) Als Gegenbeispiel wählen wir die Grammatik $G$ mit Produktionen $S \rightarrow a S \mid b S$. Es gilt also $L(G)=\emptyset$. Wir löschen nun $S$ aus der zweiten Produktion. Mit Produktionen $S \rightarrow a S \mid b$ gilt nun $L\left(G^{\prime}\right)=L\left(a^* b\right)$. 
- (c) Für $G$ nehmen wir $S \rightarrow a S \mid b$. Durch Löschen von $a$ erhalten wir $S \rightarrow S \mid b$. 
- (d) Für $G$ nehmen wir wieder $S \rightarrow a S \mid b$, und erhalten nach Löschen von $S$ die Produktionen $S \rightarrow a \mid b$.