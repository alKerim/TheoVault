Grundlagen der syntaktischen Analyse von Programmiersprachen, Parsing, Compilerbau.

# Arithmetische Ausdrücke
$$\begin{array}{l}
<\text { Expr> } \rightarrow \text { <Term }>\\
\text { <Expr> } \rightarrow \text { <Expr> }+<\text { Term }>\\
<\text { Term }>\rightarrow<\text { Factor }>\\
<\text { Term }>\rightarrow<\text { Term }>*<\text { Factor }>\\
<\text { Factor }>\rightarrow a\\
<\text { Factor }>\rightarrow(<\text { Expr }>)
\end{array}$$

# Syntaxbaum
[[Syntaxbaum]]
