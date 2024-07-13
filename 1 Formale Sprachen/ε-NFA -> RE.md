Sei $M=\left(Q, \Sigma, \delta, q_1, F\right)$ ein NFA mit $\boldsymbol{\epsilon}$-Übergänge. Wir konstruieren einen RE $\gamma$ mit $L(M)=L(\gamma)$ in zwei Schritten:

# Algorithmus
### Schritt 1 (preprocessing)
Wir transformieren $M$ in einen äquivalenten Automaten a) mit höchstens einem Endzustand, b) ohne in den Anfangszustand einkommende Übergänge und c) ohne aus dem Endzustand ausgehende Übergänge:
- Hat $q_1$ Eingangsübergänge, dann fügen wir einen neuen Zustand $q_0$ hinzu sowie einen $\epsilon$-Übergäng von $q_0$ nach $q_1$ und setzen $q_0$ als neuer Anfangsszustand.
- Enthält $F$ mehr als einen Zustand oder einen Zustand mit Ausgangsübergangen, dann fügen wir einen neuen Zustand $q_e$ sowie
   $\epsilon$-Übergänge vom jedem Zustand von $F$ zu $q_e$ und setzen $q_e$ als (einzigen) neuen Endzustand.

![[Screenshot 2024-04-28 at 20.08.51.png]]
### Schritt 2
Wiederhole so lang wie möglich:
- Solange es Übergänge $\left(q, \gamma_1, p\right)$ and $\left(q, \gamma_2, p\right)$ gibt, ersetze sie durch einen einzigen Übergang $\left(q, \gamma_1 \mid \gamma_2, q^{\prime}\right)$.
![[Screenshot 2024-04-28 at 20.09.34.png|400]]
- Wähle Zustand $q$ der weder Anfang- noch Endzustand ist.
- Hat $q$ eine Schleife $(q, \sigma, q)$,
	- ja: dann ersetze jedes Paar $(p, \gamma, q)$, $\left(q, \beta, p^{\prime}\right)$ von Übergängen mit $p \neq q \neq p^{\prime}$ (aber möglicherweise $\left.p=p^{\prime}\right)$ durch $\left(p, \gamma \sigma^* \beta, p^{\prime}\right)$, 
	- nein: ==sonst durch $\left(p, \gamma \beta, p^{\prime}\right)$.== 
- Entferne den Zustand $q$ zusammen mit all seinen eingehenden und ausgehenden Übergängen.
	Wenn $q$ eine Schleife hat
	![[Screenshot 2024-04-28 at 20.09.53.png]]
	Wenn $q$ KEINE Schleife hat (siehe [zulip](https://zulip.in.tum.de/#narrow/stream/2196-THEO-SS24-Allgemein/topic/NFA.20-.3E.20RE/near/1586010))
	![[Screenshot 2024-07-06 at 11.43.06.png]]