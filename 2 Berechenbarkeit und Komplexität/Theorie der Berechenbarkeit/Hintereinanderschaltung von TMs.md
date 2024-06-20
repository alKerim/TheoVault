Seien $M_i=\left(Q_i, \Sigma, \Gamma_i, \delta_i, q_i, \square, F_i\right), i=1,2$
Die ==sequentielle Komposition== (Hintereinanderschaltung) von $M_1$ und $M_2$ bezeichnen wir mit
$$\begin{equation*}
\longrightarrow M_1 \longrightarrow M_2 \longrightarrow
\end{equation*}$$

Sie ist wie folgt definiert:
$$\begin{equation*}
M:=\left(Q_1 \cup Q_2, \Sigma, \Gamma_1 \cup \Gamma_2, \delta, q_1, \square, F_2\right)
\end{equation*}$$
wobei (oE) $Q_1 \cap Q_2=\emptyset$ und
$$\begin{equation*}
\delta:=\delta_1 \cup \delta_2 \cup\left\{\left(f_1, a\right) \mapsto\left(q_2, a, N\right) \mid f_1 \in F_1, a \in \Gamma_1\right\}
\end{equation*}$$



# Fallunterscheidung
Sind $f_1$ und $f_2$ Endzustände von $M$ so bezeichnet
eine Fallunterscheidung, dh eine [[Turingmaschine - TM|TM]], die vom Endzustand $f_1$ von $M$ nach $M_1$ übergeht, und von $f_2$ aus nach $M_2$.
$$\begin{array}{llll}
\longrightarrow & M \xrightarrow{f_1} \quad M_1 \longrightarrow \\
& \downarrow f_2 & & \\
& M_2 & & \\
& \downarrow & &
\end{array}$$

Die folgende TM nennen wir „Band=0?" (bzw „Band $i=0$ ?“):
$$\begin{equation*}
\begin{aligned}
\delta\left(q_0, 0\right) & =\left(q_0, 0, R\right) \\
\delta\left(q_0, \square\right) & =(j a, \square, L) \\
\delta\left(q_0, a\right) & =(\text { nein, } a, N) \quad \text { für } a \neq 0, \square
\end{aligned}
\end{equation*}$$
wobei $j a$ und nein Endzustände sind.



# Schleife
Analog zur Fallunterscheidung kann man auch eine TM für eine Schleife konstruieren
$$\begin{aligned}
\longrightarrow & \text { Band } i=0 ? \quad \xrightarrow{j a} \\
& \uparrow \downarrow \text { nein } \\
& M
\end{aligned}$$
die sich wie while Band $i \neq 0$ do $M$ verhält.

Moral: Mit TM kann man imperativ programmieren:
![[Screenshot 2024-06-17 at 14.37.16.png|100]]

# Mini Programmsprachen
$$\begin{array}{l}
\text { WHILE } \equiv \text { strukturierte Programme } \\
\text { mit while-Schleifen } \\
\text { GOTO } \equiv \text { Assembler } \\
\end{array}$$
[[WHILE]]
[[GOTO]]
