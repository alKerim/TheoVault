Überbau enge ist überabzählbar wenn sie nicht [[abzählbar]] ist.


# Beispiel
Die Menge aller Funktionen $\mathbb{N} \rightarrow\{0,1\}$ ist überabzählbar.
	Beweis:
	Indirekt. Nimm an, die Menge der Funktionen sei abzählbar.

|          |    0     |    1     |    2     |    3     | $\ldots$ |
| :------: | :------: | :------: | :------: | :------: | :------: |
|  $f_0$   |  ==0==   |    1     |    1     |    0     | $\ldots$ |
|  $f_1$   |    1     |  ==0==   |    0     |    0     | $\ldots$ |
|  $f_2$   |    0     |    0     |  ==1==   |    0     | $\ldots$ |
|  $f_3$   |    0     |    0     |    1     |  ==0==   | $\ldots$ |
| $\vdots$ | $\vdots$ | $\vdots$ | $\vdots$ | $\vdots$ | $\ddots$ |

Eine Funktion $f$, die nicht in der Tabelle ist: $\neg$ Diagonale! 
$f \quad \begin{array}{llllll}1 & 1 & 0 & 1 & \ldots\end{array}$ 
Widerspruch!
Formal: Sei $f(i):=1-f_i(i)$. Dann $f \neq f_i$ für alle $i$, da $f(i) \neq f_i(i)$.

