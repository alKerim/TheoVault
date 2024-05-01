
# Algorithm
### Schritt 1 (preprocessing)
Wir wenden folgende Ersetzungsregeln so lange wie möglich auf $\gamma$ an:
$$\begin{array}{lll}
\gamma \emptyset \rightsquigarrow \emptyset & \gamma \mid \emptyset \rightsquigarrow \gamma & \emptyset^* \rightsquigarrow \boldsymbol{\epsilon} \\
\emptyset \gamma \rightsquigarrow \emptyset & \emptyset \mid \gamma \rightsquigarrow \gamma &
\end{array}$$

Die Regeln erhalten die Sprache des regulären Ausdrucks. Das Endergebnis $\gamma^{\prime}$ ist entweder $\emptyset$ (z.B. wenn $\gamma=\emptyset \emptyset$ ) oder ein regulärer Ausdruck ohne Vorkommnisse von $\emptyset$ (z.B. wenn $\gamma=a \mid \emptyset$ ). Im ersten Fall setzen wir $N$ als der NFA mit nur einen Zustand, keine Endzustände und keine Übergänge. Im zweiten Fall machen wir mit Schritt 2 weiter.

### Schritt 2
Wir wenden folgende Transformationsregeln so lange wie möglich auf den Automaten ![[Screenshot 2024-04-28 at 20.05.29.png|100]]an.
![[Screenshot 2024-04-28 at 20.05.09.png]]
Beachte: $q=p$ ist möglich und sowohl $q$ wie auch $p$ können Anfang oder Endzustände sein!.
Die Regeln erhalten die Sprache. (Übung!)
Das Endergebnis ist ein NFA mit $\epsilon$-Übergängen.



# Beispiele
### Beispiel 1
$\text { Betrachte den regulären Ausdruck }\left(a^* b^* \mid c\right)^* d \text {. }$
![[Screenshot 2024-04-28 at 20.06.32.png|400]]


