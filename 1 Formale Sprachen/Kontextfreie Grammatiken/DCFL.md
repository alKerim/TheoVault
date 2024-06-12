Eine [[Kontextfreie Sprache|CFL]] heißt deterministisch (DCFL) gdw sie von einem [[DPDA]] akzeptiert wird.
	Man kann zeigen: Die CFL $\left\{w w^R \mid w \in\{0,1\}^*\right\}$ ist nicht deterministisch.


# Fakten
Da man jeden [[DFA - Deterministische endliche Automaten|DFA]] leicht mit einem [[DPDA]] simulieren kann:
	Jede [[regulär|reguläre Sprache]] ist eine DCFL.
![[inhärent mehrdeutig#^d29d56]]



# Beispiele
#### Beispiel 1: Nicht-Deterministische CFL
Die DCFLs sind eine echte Teilklasse der CFLs.
Hier ist eine konkrete Sprache in CFL\\DCFL:
Sei $L_{w w}:=\left\{w w \mid w \in\{a, b\}^*\right\}$.
Dann ist $L:=\{a, b\}^* \backslash L_{w w}$ eine CFL aber keine DCFL.
	$L$ wird von folgender CFG erzeugt (ohne Beweis):
$$\begin{equation*}
\begin{aligned}
S \rightarrow A B|B A| A \mid B \\
A \rightarrow C A C|a \quad B \rightarrow C B C| b \quad C \rightarrow a \mid b
\end{aligned}
\end{equation*}$$

Wäre $L$ eine DCFL, dann auch $\bar{L}=L_{w w}$ (wegen Satz 4.65). Aber mit dem Pumping Lemma kann man zeigen, dass $L_{w w}$ keine CFL ist, und daher erst recht keine DCFL.

