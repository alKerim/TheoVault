Lex und Yacc sind Werkzeuge, die in der Informatik verwendet werden, um lexikalische Analysegeräte (Lex) und Parser (Yacc) zu generieren. Diese Werkzeuge sind ein integraler Bestandteil der Entwicklung von Compilern und Interpretern und überbrücken die Lücke zwischen textueller Eingabe und maschinenverständlichem Code.

## Lex

"lexikalischer Analysator" Lex, oder ein Lexer (lexikalischer Analysator), ist ein Werkzeug, das rohen Eingabetext aufnimmt und in bedeutungsvolle Einheiten, sogenannte Tokens, zerlegt. Lex selbst ist kein vollständiger [[recognizer]] oder [[Parser]]; es konzentriert sich hauptsächlich darauf, Muster im Text zu erkennen, um Tokens wie Schlüsselwörter, Zahlen, Identifikatoren und Operatoren zu identifizieren. Es befasst sich mit den lexikalischen Elementen und kann in dem Sinne als Recognizer betrachtet werden, dass es diese Muster erkennt, aber es analysiert nicht die Struktur der Eingabe gemäß Grammatikregeln.

## Yacc
"Yet Another Compiler-Compiler"
Yacc ist ein Werkzeug, das die ==von Lex produzierten Tokens nimmt== und einen ==[[Parser]] generiert==. Der Parser verwendet diese Tokens, um die syntaktische Struktur der Eingabe basierend auf einem bestimmten Satz von Grammatikregeln (normalerweise in Form einer kontextfreien Grammatik spezifiziert, Backus-Naur Form) zu überprüfen und zu interpretieren. 
Yacc baut im Wesentlichen einen Parser, der eine Art Recognizer ist, der nicht nur erkennt, ob eine Zeichenfolge zu einer Sprache gehört, sondern auch eine syntaktische Analyse basierend auf der [[Grammatik]] durchführt.