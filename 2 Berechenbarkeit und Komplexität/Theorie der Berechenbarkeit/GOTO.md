Ein GOTO-Programm ist eine Sequenzen von markierten Anweisungen
$$\begin{equation*}
M_1: A_1 ; M_2: A_2 ; \ldots ; M_k: A_k
\end{equation*}$$
(wobei alle Marken verschieden und optional sind)
#theo/basics 
Mögliche Anweisungen $A_i$ sind:
$$\begin{equation*}
\begin{array}{l}
x_i:=x_j+n \\
x_i:=x_j-n \\
\text { GOTO } M_i \\
\text { IF } x_i=n \text { GOTO } M_j \\
\text { HALT }
\end{array}
\end{equation*}$$

Die Semantik ist wie erwartet.



# GOTO-Berechenbarkeit
![[WHILE#^d63317]]
