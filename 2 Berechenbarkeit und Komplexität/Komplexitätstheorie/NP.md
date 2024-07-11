#theo/definition
$\mathrm{NP} =$ die von einer [[NTM]] in polynomieller Zeit lösbaren Probleme 

Für in exponentieller Zeit lösbarer Probleme gilt (gilt NICHT für NP Probleme):
	In exponentieller Zeit lösbar (s. Simulation NTM durch [[DTM|DTM]])


$\text { NP }:=\bigcup_{p \text { Polynom }} \operatorname{NTIME}(p(n))$
[[NTIME(f(n))]]

# Entscheidbarkeit
Alle Probleme in NP sind entscheidbar. 
Wie in Vorlesung[^1] argumentiert, gibt es für jedes Problem in NP zumindest eine Entscheidungsprozedur mit Laufzeit $2^{p(n)}$ ^19ece9

# Zeit
![[NP#^19ece9]]

# Bekannt
- Es gibt Probleme, die schwerer sind als NP (aber die behandeln wir in Theo nicht, interessieren uns nicht)


# Beispiele
- [[HAMILTON]] $\in$ NP, aber HAMILTON $\not \in$ [[P]]




___
[^1]: Vorlesung vom 8.7.24