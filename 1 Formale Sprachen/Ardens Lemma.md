Sind $\alpha, \beta$ und $X$ reguläre Ausdrücke mit $\epsilon \notin L(\alpha)$, so gilt
$$\begin{equation*}
X \equiv \alpha X \mid \beta \quad \Longrightarrow \quad X \equiv \alpha^* \beta
\end{equation*}$$



# Wichtig

## wichtig a*
#theo/wichtig 
Folgt aus der Gleichung $X \equiv(a \mid \epsilon) X \mid a$, dass $X \equiv(a \mid \epsilon)^* a$ ? Beweisen Sie die Implikation oder geben Sie ein Gegenbeispiel an (mit kurzer Begründung).

Gegenbeispiel: $X \equiv a^*$ ist eine Lösung von $X \equiv(a \mid \epsilon) X \mid a$ aber $a^* \not \equiv(a \mid \epsilon)^* a \equiv$ $a^{+}$

#### Erklärung ([zulip](https://zulip.in.tum.de/#narrow/stream/2183-THEO-SS24-Blatt-03/topic/H3.2E2b/near/1567058))
Wenn wir es in die erste Gleichung einsetzen:
$$\begin{equation*}
\begin{array}{c}
a^* \equiv(a \mid \epsilon) a^* \mid a \\
\Leftrightarrow a^* \equiv a a^*\left|a^*\right| a \\
\Leftrightarrow a^* \equiv a^*
\end{array}
\end{equation*}$$
Dagegen die zweite:
$$\begin{equation*}
\begin{array}{c}
a^* \equiv(a \mid \epsilon)^* a \\
\Leftrightarrow a^* \equiv a^{+}
\end{array}
\end{equation*}$$
Somit gilt für $X=a^*$ die erste Gleichung und die zweite nicht.


### wichtig $\Sigma^*$
[zulip](https://zulip.in.tum.de/#narrow/stream/2196-THEO-SS24-Allgemein/topic/Ardens.20Lemma.20.28Retake22.20Aufg.2E.204b.29.20.29)
Bei der zweiten Gleichung:
Wieso ist diese Gleichung äquivalent zu $\Sigma^*$ ?
Ardens Lemma lässt sich hier ja auch prinzipiell nicht anwenden laut Definition aus VL weil $\epsilon$ in $a^*$ enthalten ist:
Sind $\alpha, \beta$ und $X$ reguläre Ausdrücke mit $\epsilon \notin L(\alpha)$, so gilt
$$\begin{equation*}
X \equiv \alpha X \mid \beta \quad \Longrightarrow \quad X \equiv \alpha^* \beta
\end{equation*}$$

Wenn $X$ äquivalent $\mathrm{zu} \Sigma^*$ wäre, dann müsste ja zB $b$ eine Lösung der Gleichung sein, was hier jetzt nicht erkenntlich wird für mich?

Aufgabe in Frage:
![[Pasted image 20240709202641.png]]

#### Antwort
Die Gleichung ist nicht äquivalent zu $X=\Sigma^*$, sondern $X=\Sigma^*$ ist eine Lösung. Dies kann man überprüfen, indem man es einsetzt.

Es gibt unendlich viele Lösungen, ja. Du bekommst aber keine Wörter als Lösung, sondern Sprachen. $X=\Sigma^*$ ist eine Lösung. $X=\{b\}$ ist keine Lösung.
