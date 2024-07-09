Man kann eine Formel ohne gewisse Struktur durch Äquivalenzumformungen in beispielsweise [[KNF]] umformen.


# Umformungen

### Idempotenz
$(A \wedge A) \leftrightarrow A$
$(A \vee A) \leftrightarrow A$

### Negation
$A \Longrightarrow B$
$\neg B \Longrightarrow \neg A$

### gdw zu Implikation
$(D \leftrightarrow A \wedge B) \equiv (D \rightarrow A \wedge B) \wedge(A \wedge B \rightarrow D)$


### Implikation zu $\cup$, $\cap$
$$\begin{aligned}
\equiv & (D \rightarrow A \wedge B)\\
\equiv & (\neg D \vee(A \wedge B))\\
\end{aligned}$$
und
$$\begin{aligned}
\equiv  (A \wedge B \rightarrow D) \\
\equiv (\neg(A \wedge B) \vee D) \\
\end{aligned}$$


# Beispiel
$$\begin{aligned}
& (D \leftrightarrow A \wedge B) \\
\equiv & (D \rightarrow A \wedge B) \wedge(A \wedge B \rightarrow D) \\
\equiv & (\neg D \vee(A \wedge B)) \wedge(\neg(A \wedge B) \vee D) \\
\equiv & (\neg D \vee A) \wedge(\neg D \vee B) \wedge(\neg A \vee \neg B \vee D)
\end{aligned}$$