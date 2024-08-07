#theo/definition
![[P]]

![[NP]]

# Frage
$\mathrm{P} = \mathrm{NP}$ ?




# gdw's
Es gilt $P=N P$ gdw ein [[NP-vollständig|NP-vollständiges]] Problem in $P$ liegt.


# Warum interessieren wir uns für $\mathrm{NP}$ 
Es gibt in der Informatik sehr viele Probleme bei denen es eine große Anzahl an Lösungen haben. 
Das Problem hierbei ist, dass es exponentiell viele Lösungen gibt.


# Ist wichtig
- weil viele praktisch relevante Such- und Optimierungsprobleme in NP liegen
- und alle schnell lösbar wären wenn $P=N P$.



# Falls P=NP
Dann [[NP]] = [[P]] = [[NP-vollständig]]
Außer $\Sigma^*$ und $\emptyset$ 

Dann 
- gilt: $3-S A T \leq_p\left\{0^n 1^n 0^n \mid n \in \mathbb{N}\right\}$
- gilt NICHT: $\left\{0^n 1^n 0^n \mid n \in \mathbb{N}\right\} \leq_p 3-S A T$

Für zwei beliebige Probleme A,B (also egal ob P oder NP)
muss nun immer gelten, dass $A \leq_{p}B$ 
![[Screenshot 2024-07-14 at 10.20.23.png|400]]

# Falls P$\neq$NP
Alle

![[Screenshot 2024-07-08 at 18.05.20.png|500]]
