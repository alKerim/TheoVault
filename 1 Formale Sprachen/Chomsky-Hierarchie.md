Benannt nach [[Noam Chomsky]], der die Hierarchie erfunden hat.

Eine Grammatik $G$ ist vom
- [[Typ 0]] immer. ^2fe2b9
- Typ 1 falls jede Produktion $\alpha \rightarrow \beta$ außer $S \rightarrow \epsilon$ $|\alpha| \leq|\beta|$ gilt und, wenn $S \rightarrow \epsilon$ eine Produktion ist, dann kommt $S$ in $\beta$ nicht vor
- Typ 2 falls $G$ vom Typ 1 ist und für jede Produktion $\alpha \rightarrow \beta$ gilt $\alpha \in V$.
- Typ 3 falls $G$ vom Typ 2 ist und für jede Produktion $\alpha \rightarrow \beta$ außer $S \rightarrow \epsilon$ gilt $\beta \in \Sigma \cup \Sigma V$.

Offensichtlich:
$\operatorname{Typ} 1 \subset \operatorname{Typ} 2 \subset \operatorname{Ty} 1 \subset \operatorname{Typ} 0$


____

# Genauere Erläuterung der Sprachen

| Typ   | Grammatik                  | Sprachen                     |
| ----- | -------------------------- | ---------------------------- |
| Typ 3 | Rechtslineare Grammatik    | [[Reguläre Sprachen]]        |
| Typ 2 | Kontextfreie Grammatik     | Kontextfreie Sprachen        |
| Typ 1 | Kontextsensitive Grammatik | Kontextsensitive Sprachen    |
| Typ 0 | Phrasenstrukturgrammatik   | Rekursiv aufzählbare Sprache |
$L(\operatorname{Typ} 3) \subset L(\operatorname{Typ} 2) \subset L(\operatorname{Typ} 1) \subset L(\operatorname{Typ} 0)$


- Um zu beschreiben was ein [[Token]] ist reichen wir Rechtslineare Grammatiken.
- Um zu beschreiben welche Sequenzen von Tokens Programme sind brauchen wir kontextfreie Grammatiken (hierzu Syntax von Token-folgen: [[Lexikalische Grammatik]])

