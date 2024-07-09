
# Probleme die nicht entscheidbar sind
Für [[Kontextfreie Grammatiken|CFGs]] sind folgende Probleme nicht [[entscheidbar]]:

**Äquivalenzproblem**
![[Äquivalenzproblem#^06dfa8]]

![[Schnittproblem]]

![[Regularitätsproblem]]

![[Mehrdeutigkeitsproblem]]

#### Nicht entscheidbare [[Kontextfreie Grammatiken|CFG]] Probleme
- Für [[DFA - Deterministische endliche Automaten|DFAs]] ist fast alles entscheidbar:
$$\begin{equation*}
L(A)=\emptyset, L(A)=L(B), \ldots
\end{equation*}$$
- Für [[Turingmaschine - TM]] ist fast nichts entscheidbar:
$$\begin{equation*}
L(M)=\emptyset, L\left(M_1\right)=L\left(M_2\right), \ldots
\end{equation*}$$
- Für CFGs ist manches entscheidbar $(L(G)=\emptyset, w \in L(G))$, und manches unentscheidbar.

- Für CFGs $G_1, G_2$ sind folgende Probleme unentscheidbar:$$\begin{equation*}
	\begin{array}{l}
	P_1: \text { Ist } L\left(G_1\right) \cap L\left(G_2\right)=\emptyset \text { ? } \\
	P_2: \text { Ist }\left|L\left(G_1\right) \cap L\left(G_2\right)\right|=\infty \text { ? } \\
	P_3: \text { Ist } L\left(G_1\right) \cap L\left(G_2\right) \text { kontextfrei? } \\
	P_4: \text { Ist } L\left(G_1\right) \subseteq L\left(G_2\right) ? \\
	P_5: \text { Ist } L\left(G_1\right)=L\left(G_2\right) \text { ? }
	\end{array}
	\end{equation*}$$
Für eine CFG G sind folgende Probleme unentscheidbar:
1. Ist $G$ [[mehrdeutig (theo)]]?
2. Ist $L(G)$ [[regulär]]?
3. Ist $L(G)$ deterministisch ([[DCFL]])?

Für eine CFG $G$ und einen RE $\alpha$ ist $L(G)=L(\alpha)$ unentscheidbar.

From Kahoot
- Seien $\mathrm{G}_1, \mathrm{G}_2$ CFGs. Ist $\mathrm{L}\left(\mathrm{G}_1\right) \cap \mathrm{L}\left(\mathrm{G}_2\right)$ kontextfrei?
- Seien $G_1, G_2$ CFGs. Gilt $L\left(G_1\right) \neq L\left(G_2\right)$ ?


# Halteprobleme die nicht entscheidbar sind
[[Spezielles Halteproblem]]





____
Related: [[entscheidbar]]