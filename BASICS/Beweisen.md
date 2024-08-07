
# Beweisen dass eine Aussage wahr ist
## $A \subseteq B$
Wähle ein beliebiges $x \in A$ und zeige $x \in B$.
#### Beispiel Für Grammatiken ($L(G) \subseteq L$ und $L \subseteq L(G)$) 
#theo/strukturelleinduktion
(Tutorium 5) von [Ü5.6](https://teaching.model.in.tum.de/2024ss/theo/ex/ue05-nosolution.pdf?key=GCkpL14q) und Lösung von [Adrians Tutorfolien](https://zulip.in.tum.de/user_uploads/2/f9/AigI48jraioH3lprdi_rlr0q/Theo-S05.pdf) 

Geg.:   $\begin{array}{l}L=\left\{a^n b^n \mid n \in \mathbb{N}\right\} \\ G: S \rightarrow a S b \mid \varepsilon\end{array}$
Ges.: z.z.   $L(G)=L$

##### $L(G) \subseteq L:$
Wir zeigen $\quad \forall w \in \Sigma^*: \quad \overbrace{S \rightarrow_G^* w}^{w \in L(G)} \Rightarrow w \in L$
per Induktion über die Erzeugung von w.
Fallunterscheidung
- Fall $S \rightarrow \varepsilon:$ Es gilt sofort $\varepsilon \in L$.
- Fall $S \rightarrow a S b:$ Sei $w \in \Sigma^*$ mit $S \rightarrow a S b \rightarrow_{G^*}awb$.
	Somit gilt $S \rightarrow_G^* w$ und damit $w \in L(G)$. Per I.H. erhalten wir außerdem $w \in L$. Somit existiert ein $n \in \mathbb{N}_0$, sodass $w=a^n b^n$. wir fixieren ein solches $n$.
	Dadurch gilt aber auch
	$$\begin{equation*}
	a w b=a a^n b^n b=a^{n+1} b^{n+1} \in L \text {. }
	\end{equation*}$$


##### $L \subseteq L(G)$: (Ind. Beweis über die Länge) 
(wir zeigen für alle $w \in L$, dass es auch in $L(G)$ produziert werden kann)
Induktion über die Länge:
$\forall w \in \sum^*: w \in L \Rightarrow w \in L(G)$ durch starke Induktion über die Länge $n$ des Wortes $w$ zeigen.
- Fall $n=0$: Es folgt $w=\varepsilon$ und $S \rightarrow_G \varepsilon$.
- Fall $n=1$ : Es folgt $w=a$ oder $w=b$. 
	Jedoch $a, b \notin L$. 
	Widerspruch zur Annahme w $\in L$ !
- Fall $n \geq 2:$ Falls $n$ ungerade, dann $w \notin L$. Widerspruch! 
	Somit is $n$ gerade.
	Sei: $w=a^{i+1} b^{i+1}=a u b$ mit $i=\frac{n}{2}-1$ $u=a^i b^i$.
	Dadurch gilt $\quad|u|=2 i=n-2<n$.
	Nach I.H. existiert also $S \rightarrow_a^7 u$.
	Damit $S \rightarrow_G aSb \rightarrow_{G^*}aub$  $=w$.

#### Edge-Case $L(G) \subseteq \Sigma^*$
#theo/cheatsheet 
Trivial weil:
$\forall w \in L(G)$ gilt $w \in \Sigma^*$, da $\Sigma^*$ die Menge aller möglichen Wörter über $\Sigma$ ist.


#### Edge-Case $\Sigma^* \subseteq L(G)$
Wir zeigen $\Sigma^* \subseteq L_G(T)$ per Induktion über die Wortlänge $n$ von $w \in \Sigma^*$. Im Fall $n=0$ gilt $w=\epsilon$ und $T \rightarrow \varepsilon$.
**Ind. Hypothese:** Im Fall $w \in \Sigma^{n+1}$ erhalten wir als Induktionshypothese, dass 
	$\Sigma^n \subseteq L_G(T)$. 
Sei nun $x \in \Sigma$ und $v \in \Sigma^n$ mit $w=x v$. 
Per I.H. gibt es eine Ableitung $T \rightarrow^* v$. 
Falls $x=a$, folgt $T \rightarrow a T \rightarrow^* a v$. Falls $x=b$, folgt $T \rightarrow b T \rightarrow^* b v$.

_____

## $A=B$
Zeige erst $A \subseteq B$ und dann $B \subseteq A$.

_____
## $A \Rightarrow B:$
Nimm an, dass $A$ gilt, und zeige, dann unter dieser Annahme auch B gilt.
Hier geht auch [[##Beweis durch Kontraposition]]
_____
## $A \Leftrightarrow B$
Zeige erst $A \Rightarrow B$ and dann $B \Rightarrow A$.


_____
## "blabla" $\Rightarrow X \subseteq Y$ ?
Wie beweist man "blabla" $\Rightarrow X \subseteq Y$ ?
$\Rightarrow$ Annahme: "blabla"
Sei $w \in X$ 
$\Rightarrow \ldots$
$\Rightarrow^{Ann.} \ldots$
$\Rightarrow \ldots$
$\Rightarrow w \in Y$

## Induktion über $n \in \mathbb{N}_0$ :
Zeige zuerst, dass die Aussage for $n=0$ gill anschließen, nimm an, dass die Aussage für n gilt, und zeige, dass unter dieser Annahme die Aussage auch for $n+1$ gilt.


_____
## Beweis durch Widerspruch:
Nimm die Negation der Aussage an und führe dies zu einem Widerspruch.

_____
## Beweis durch Kontraposition
Falls $A \Rightarrow B$ zu zeigen ist, zeige $\neg A \Leftarrow \neg B$ oder beziehungsweise schöner geschrieben von links nach recht $\neg B \Rightarrow \neg A$.

_____
# Widerlegen einer Aussage
## Angeben eines Gegenbeispiels
Selbsterklärend.

#### Hilfsgedanken:
bspsweise: "Zeigen oder widerlegen Sie: $\overline{L}$ regulär"
	Kennen wir $L$ ? Ist $L$ regulär ? Wenn $L$ nicht regulär, dann $\overline{L}$ auch nicht regulär, wegen [[Abschlusseigenschaften regulärer Sprachen]]


# Formaler Widerspruchsbeweis
Formaler Widerspruchsbeweis
Wir nehmen an, dass es einen DFA M mit weniger all $2^n$ Zuständen gibt.
Se: $w \neq v$ aber $\quad \hat{\delta}(q_0, w)=\hat{\delta}\left(q_0, v\right)=p$.
Sei $w_i=a$ und $v_i=b$.
Sei $x=w a^i \quad$ und $y=v a^i$.

Dann $\quad x \in B_n$, weil $x=\underbrace{w_1 \ldots w_i}_i \underbrace{w_{i+n} \cdots w_n}_n \underbrace{i}_i$, und $y \notin B_n$.

## Negieren und [[#Beweisen dass eine Aussage wahr ist]]



______
# Andere Guides+Quellen zum Beweisen-Lernen
[[how-to-prove-it_book.pdf]] -> [Download zum PDF](https://users.metu.edu.tr/serge/courses/111-2011/textbook-math111.pdf)


____

# Konkrete Beweise
### Zeigen Sprache nicht regulär
[[regulär#nicht-regulär]]

### Zeigen Sprachen ungleich
[[Sprachen Unterscheidbar#Sprachen unterscheiden sich beweisen]]



________
# Begründen unterschied
[[Begründen vs. Beweisen]]
