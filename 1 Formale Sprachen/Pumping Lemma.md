# Pumping Lemma für reguläre Sprachen
Wie zeigt man, dass eine Sprache ==nicht [[regulär]]== ist?

Sei $R \subseteq \Sigma^*$ regulär. Dann gibt es ein $n>0$, so dass sich jedes $z \in R$ mit $|z| \geq n$ so in $z=u v w$ zerlegen lässt, dass
- $v \neq \epsilon$,
- $|u v| \leq n$, und
- $\forall i \geq 0 . u v^i w \in R$.

Fall 1: Alle drei Bedingungen sind true: KEINE Aussage möglich!!
Fall 2: Eine oder mehr der Bedingungen treffen nicht zu: Sprache ist nicht regulär!!

### Wichtig:
Es gibt nicht-reguläre Sprachen, für die das Pumping-Lemma gilt!
$\Rightarrow$ Pumping-Lemma hinreichend aber nicht notwendig um Nicht-Regularität zu zeigen.

Sprache $L$ regulär $\Rightarrow$ Pumping-Lemma gilt



### Easy Explanation
Wir nehmen Bedingung 1 und 2,
also $v \neq \epsilon$, und $|u v| \leq n$,
und wählen $v,n$ so dass die Bedingungen 1 und 2 erfüllt sind.

Dann wählen wir zwei weitere Sachen:
1. (ein spezifisches $u$) und ($v$ ist sowieso schon $v=\epsilon$)
2. und ein $i$ , sodass $uv^{i}w \notin R$

Wir wählen also mit Absicht oder Versuchen ein Wort zu wählen durch ändern von $i$ sodass es nicht mehr in der ursprünglichen Sprache ist.


### Logische Struktur: für jede reguläre Sprache $R$
- $\exists n>0 . \forall z \in R \text { mit }|z| \geq n . \exists u, v, w . z=u v w \wedge \ldots$

- Spielbasierte Formulierung.
	Sei $R$ eine Sprache (regulär oder nicht). Eine Partie des $R$-Spiels zwischen zwei Spielern läuft so:
	- Spieler I wählt eine Zahl $n>0$
	- Spieler II wählt ein Wort $z \in R$ mit $|z| \geq n$
	- Spieler I wählt eine Zerlegung $u v w$ von $z$.
	Spieler I gewinnt, wenn $u v w$ die gewünschten Eigenschaften erfüllt, sonst gewinnt Spieler II.

- Das Pumping Lemma sagt: für jede reguläre Sprache $R$, Spieler I hat eine Gewinnstrategie im $R$-Spiel, d.h., wenn er richtig spielt, dann gewinnt er jede Partie.
- Gewinnstrategie für Spieler I: Regeln, um erst eine Pumping-Lemma-Zahl $n$, und dann eine gute Zerlegung $u v w$ zu wählen (eine Zerlegung, die die Eigenschaften erfüllt).



## Beispiele
### Beispiel 1
Die Sprache $\{a^i b^i \mid i \in \mathbb{N}\}$ ist nicht regulär.
Beweis:
Angenommen, $L$ sei doch regulär.
Sei $n$ eine Pumping-Lemma-Zahl für $L$.
Wähle $z=a^n b^n \in L$.
Jede gute Zerlegung $u v w$ von $z$ erfüllt
$u, v \in\{a\}^*$ (weil $|u v| \leq n$ ) und $v \neq \epsilon$.
"Endliche Automaten können nicht unbegrenzt zählen"
Ist die Sprache $\{a^n b^n \mid n \leq 10^6\}$ regulär?

### Beispiel 2
$L=\{0^{m^2} \mid m \geq 0\}$ ist nicht regulär.
Beweis:
Angenommen, $L$ sei doch regulär.
Sei $n$ eine Pumping-Lemma-Zahl für $L$.

Wähle $z=0^{n^2} \in L$. Sei $u v w$ eine Zerlegung von $z$ mit
$1 \leq|v| \leq|u v| \leq n$

Wir zeigen $u v^2 w \notin L$. D.h., wir beweisen, dass $\left|u v^2 w\right|$ keine Quadratzahl ist. 
Mit
$n^2=|z|=|u v w|<\left|u v^2 w\right| \leq n^2+n<n^2+2 n+1=(n+1)^2$
gilt:
$n^2<\left|u v^2 w\right|<(n+1)^2$. Zwischen $n^2$ und $(n+1)^2$ liegt keine Quadratzahl.

## Templates Adrian
#### Schema wenn wir PL für L beweisen wollen (Also L das PL erfüllt):
1. Wir wählen ein konkretes $n>0$. (Also beispielsweise $n=3$)
2. Wir fixieren ein beliebiges $z \in L$ mit $|z| \geq n$. (Also beispielsweise $z=ab^mb^m$)
3. Wir geben für $z$ eine passende Zerlegung $z=u v w$ an.
4. Wir zeigen explizit, dass
	1. $v \neq \varepsilon$
	2. $|u v| \leq n$
	3. $\forall i \geq 0: u v^i w \in L$
Zum üben/verstehen: [H3.4c)](https://teaching.model.in.tum.de/2024ss/theo/ex/ha03-solution.pdf?key=nSFcLMvc)


#### Schema, wenn wir zeigen wollen, dass $L$ das PL nicht erfüllt:
1. Wir nehmen an dass $L$ regulär ist.
2. Wir fixieren sin beliebiges $n>0$.
3. Wir geben in konkretes $z$ in Abhängigkeit von $n$ an, sodass $|z| \geq n$ und $z \in L$.
4. Wir zeigen für jede beliebige Zerlegung $z=u v w$, dass mind. einer der drei Bedingungen nicht gilt:
	1. $v \neq \varepsilon$
	2. $|uv| \leq n$
	3. $\forall i \geq 0: u v^i w \in L$


## Template für PL reguläre Sprachen
Für
$L_1=\left\{a^n b^n a^m b^m \mid n, m \in \mathbb{N}\right\}$

(Der Beweis funktioniert analog für alle vier Sprachen. (2022Endterm Aufgabe 6)) 
Wir wählen $L_1$. 
Wir führen einen Widerspruchsbeweis und nehmen an, dass $L_1$ regulär wäre. 
Dann gilt die Aussage des Pumping-Lemma (PL) für reguläre Sprachen. 
Sei $n \in \mathbb{N}$ die PL-Zahl. 
Nun wählen wir das Wort $z:=a^n b^n a^n b^n$. 
Nach PL existiert eine Zerlegung $z=u v w$. 

Es gilt $|u v| \leq n$ und $v \neq \varepsilon$, 
wir können also $v=a^i$ schreiben, für ein $i>0$. 
Nun gilt auch $u v^0 w \in L_1$, aber $u w=a^{n-i} b^n a^n b^n \notin L$, da $n-i \neq n$. 
Dies ist ein Widerspruch, $L_1$ kann somit nicht regulär sein.



# Pumping Lemma für kontextfreie Sprachen
[[Pumping Lemma für kontextfreie Sprachen]]