---
title: "Fehlspezifikation von Belohnungen"
date: 2023-10-14T12:41:22+02:00
summary: Es ist schwierig, eine Belohnungsfunktion zu erstellen, die
  genau das widerspiegelt, was wir wollen.
---

![Fehlspezifikation von Belohnungen](/king-midas.png 'Fehlspezifikation von Belohnungen ist eine Fehlerart bei der Erstellung von KI-Modellen, verursacht durch die inhärente Schwierigkeit, unsere Absichten sauber zu formalisieren. Ein berühmtes fiktionales Beispiel ist König Midas, der sich wünschte, dass alles, was er berührte, zu Gold wurde.')

# Grundlagen

Es ist schwierig, einen Wunsch so klar zu formalisieren, dass er unsere Absichten vollständig widerspiegelt. Ein berühmtes fiktionales Beispiel ist die Geschichte von König Midas, der sich wünschte, dass alles, was er berührte, zu Gold wird. Das scheint oberflächlich betrachtet ein effektiver Weg zu sein, um reich zu werden, führt jedoch der Sage nach zu einigen eher unbeabsichtigten Nebenwirkungen, wie zum Beispiel, dass seine Liebsten zu Gold wurden, sowie jegliches Essen, das er zu sich nehmen wollte.

Obwohl die Nachteile dieses speziellen Wunsches offensichtlich erscheinen mögen, hat die Forschung im maschinellen Lernen gezeigt, dass ähnliche Dinge recht häufig in der Praxis passieren, weil es überraschend schwierig ist vorherzusehen, ob eine gegebene Belohnungsfunktion (die zum Trainieren der KI verwendet wird) tatsächlich dazu führt, dass sich die KI auf wünschenswerte Weise verhält, oder ob sie tatsächlich zu völlig unerwarteten und unerwünschten Verhaltensweisen führen kann, die aufdecken, dass die Belohnungsfunktion einige Lücken oder Schlupflöcher aufweist.

# Weiterführend

Fehlspezifikation von Belohnungen ("reward misspecification") ist eine Fehlerart bei der Erstellung von KI-Modellen, die auf der inhärenten Schwierigkeit fußt, eine Belohnungsfunktion (oder Verlustfunktion) zu spezifizieren, die Belohnungen für Aktionen oder Weltzustände zuweist, die genau das widerspiegeln, was wir wollen. Diese Funktionen werden verwendet, um die KI zu einem hoffentlich nützlichen Verhalten zu steuern. Dies ist jedoch oft problematisch, weil es sehr schwierig ist, eine solche Funktion zu konstruieren, die wirklich gut mit dem übereinstimmt, was wir *tatsächlich* wollen. Dies liegt daran, dass unsere Ziele und Wünsche eine Menge versteckter Komplexität aufweisen.

Nehmen wir an, wir bitten jemanden, uns einen Kaffee zu holen. Das klingt einfach, aber es gibt tatsächlich eine Menge impliziter Einschränkungen. Zum Beispiel kann es akzeptabel sein, dass die Person (oder KI) ein wenig Geld ausgibt, um das Ziel zu erreichen - aber wahrscheinlich keine 50 Euro. Wir hoffen implizit, dass diese Aktion nicht mehr als ein paar Minuten dauert, und wir den Kaffee nicht erst in zwei Wochen bekommen. Außerdem sollte kein signifikanter Kollateralschaden entstehen, und die Küche sollte nicht in Unordnung hinterlassen werden. In [The Hidden Complexity of Wishes](https://www.lesswrong.com/posts/4ARaTpNX62uaL86j6/the-hidden-complexity-of-wishes) stellt Eliezer Yudkowsky fest, dass "es keinen sicheren Wunsch gibt, der kleiner ist als eine ganze menschliche Moral". Dies erklärt im Grunde das Problem bei der Spezifizierung von Belohnungsfunktionen: Eigentlich müssen wir unsere zahllosen impliziten Einschränkungen alle explizit machen, um eine Belohnungsfunktion aufzustellen, die nicht zu unerwünschten Ergebnissen führt, wenn wir sie in einen Optimierungsprozess einbinden.

Obwohl das obige Beispiel etwas theoretisch klingen mag, gibt es tatsächlich viele dokumentierte Fälle, in denen Fehlspezifikation von Belohnungen tatsächlich dazu führte, dass KIs sich auf unerwartete und unerwünschte Weisen verhielten.

## Beziehung zu anderen Begriffen

Fehlspezifikation von Belohnungen ist eng mit dem weit verbreiteten Begriff des *Outer Misalignment* verbunden und beschreibt die Diskrepanz zwischen dem, was wir (als Ersteller einer KI) wollen, und der Belohnungs- (oder Verlust-) Funktion, die wir erstellen, um dies widerzuspiegeln. Das Gegenstück, das sogenannte *Inner Misalignment*, ist eine weitere Fehlerart der KI-Erstellung, der sich auf die Diskrepanz zwischen der Belohnungs- (oder Verlust-) Funktion und dem, was die KI tatsächlich lernt, bezieht. In der Praxis passiert oft beides: Unsere Belohnungsfunktion spiegelt nicht perfekt unsere wahren Absichten wider und die KI lernt etwas anderes als die eigentliche Belohnungsfunktion (siehe Fehlgeneralisierung von Zielen).

![Innere vs. Äußere Ausrichtung](/inner-outer-alignment.png 'Diagramm, das die Beziehung zwischen "Inner" und "Outer Alignment" zeigt')

([Quelle](https://www.lesswrong.com/posts/x2n7mBLryDXuLwGhx/technical-ai-safety-research-landscape-slides))

Es gibt auch den Begriff des "Specification Gamings", der allgemein den Prozess beschreibt, bei dem Reinforcement Learning-Agenten lernen, sich auf unerwartete Weisen zu verhalten, die hohe Belohnungen bringen. Dies kann sowohl gut als auch schlecht sein: Es kann gut sein in dem Sinne, dass die KI ein bisher unbekanntes Verhalten findet, das tatsächlich das Ziel erreicht (z.B. Ausnutzen von Schwachstellen in Videospielen). Aber recht oft ist es eher unerwünscht, da die KI Schlupflöcher in der Gestaltung der Belohnungsfunktion identifiziert und diese ausnutzt.

# Fortgeschritten

- https://course.aisafetyfundamentals.com/alignment?session=2
- "Die Auswirkungen von Fehlspezifikation von Belohnungen": https://arxiv.org/abs/2201.03544
- https://openai.com/research/learning-from-human-preferences
- https://www.deepmind.com/blog/specification-gaming-the-flip-side-of-ai-ingenuity
- Tabelle mit vielen Beispielen für Fehlgeneralisierung von Zielen: https://docs.google.com/spreadsheets/d/e/2PACX-1vRPiprOaC3HsCf5Tuum8bRfzYUiKLRqJmbOoC-32JorNdfyTiRRsR7Ea5eWtvsWzuxo8bjOxCG84dAg/pubhtml 
