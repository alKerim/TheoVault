#theo/cheatsheet 
Sei $M$ eine DTM mit $L(M) \subseteq\left\{w \# c \mid w \in \Sigma^*, c \in \Delta^*\right\}$.
- Falls $w \# c \in L(M)$, so heißt $c$ Zertifikat für $w$. 
- $M$ ist ein polynomiell beschränkter Verifikator für die Sprache $\left\{w \in \Sigma^* \mid \exists c \in \Delta^* . w \# c \in L(M)\right\}$ falls es ein Polynom $p$ gibt, so dass $\operatorname{time}_M(w \# c) \leq p(|w|)$.

---> Kommt manchmal in Quizzes vor
