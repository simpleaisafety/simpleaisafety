---
title: "Mesa-Optimierer"
date: 2023-11-25T17:35:20+02:00
summary: Manchmal kann ein Optimierungsprozess Agenten erschaffen,
  die selbst Optimierer sind.
---

![Mesa-Optimierer](/mesa-optimizers.jpg 'Deep Learning beinhaltet oft, dass menschliche KI-Forscher einen Optimierungsprozess wie Stochastic Gradient Descent verwenden, um ein KI-Modell zu trainieren, das gut darin ist, ein Trainingsziel zu erreichen. Mesa-Optimierung ist der spezifische Fall, in dem das trainierte Modell selbst ein Optimierer ist, der dann in der Welt handelt und versucht, sie in einen Zustand zu bringen, der seinem Ziel näher ist.')

# Grundlagen

Der Begriff "Mesa-Optimierung" beschreibt das Szenario, in dem ein äußerer Optimierungsprozess, wie die Trainingsphase im maschinellen Lernen, KIs erschafft, die selbst Optimierer sind. Bis heute geschieht dies in den meisten Fällen nicht, da die trainierten KIs meist in einer eher begrenzten Weise agieren, die nicht sehr nahe an einer absichtlichen Optimierung ist. Es gibt jedoch Gründe zu der Annahme, dass Mesa-Optimierer letztendlich aus dem Bereich des maschinellen Lernens hervorgehen werden, weil Menschen Gründe haben, immer mehr zu versuchen, ihre Trainingsprozesse dazu zu bringen, solche Mesa-Optimierer zu erschaffen.

Ein Beispiel für Mesa-Optimierung ist, wie die Evolution schließlich zu Menschen führte, die (auf bestimmte Weisen) selbst Optimierer sind: Wir neigen dazu, die Welt absichtlich so zu formen, dass sie unseren Präferenzen näher kommt.

Dieses Beispiel zeigt auch, warum die Möglichkeit von Mesa-Optimierern beunruhigend ist: Menschen sind in vielerlei Hinsicht nicht genau auf die "Ziele" der Evolution ausgerichtet. Verhütung ist ein Beispiel dafür. Wenn maschinelles Lernen schließlich zu ähnlich starken Mesa-Optimierern führt, gepaart mit ähnlich fehlgeleiteten Zielen, kann dies zu sehr unerwünschten Ergebnissen führen.

# Weiterführend

Viele der eher "philosophischen" Überlegungen zu den Gefahren der KI, wie die von Nick Bostrom oder Eliezer Yudkowsky, konzentrieren sich auf "Optimierer", also KIs, die die Welt auf Weisen formen, die sie einem Ziel näher bringen, unter Nutzung eines besonders starken Optimierungsvermögens. Allerdings sind die meisten heutigen KIs wahrscheinlich keine, oder zumindest noch keine besonders fähigen, "Optimierer". Ob durch Reinforcement Learning trainiert oder durch (semi-) supervised Learning, in der Praxis zeichnen sie sich häufig dadurch aus, bestimmten Verhaltensweisen zu folgen, die "zufällig" den Effekt haben, in Hinblick auf die Zielfunktion gut abzuschneiden. Das bedeutet nicht, dass sie irgendeine Art von expliziter interner Darstellung dieses Trainingsziels haben, geschweige denn, dass sie absichtlich versuchen, danach zu optimieren. Andererseits gibt es eindeutig eine gewisse Optimierung im *Training* der KIs, oft in Form von stochastischem Gradientenabstieg (SGD). Also gibt es tatsächlich meist einen Optimierer im Spiel, aber die Optimierung findet *während des Trainings* statt und nicht *während der Nutzung der KI* (wenn das Modell in der realen Welt eingesetzt wird).

Bedeutet dies, dass Bostrom und Yudkowsky in ihren Sorgen fehlgeleitet waren und trainierte KIs harmlos sein werden, da sie selbst keine Optimierer sind? Leider nein, denn hier kommen die Mesa-Optimierer ins Spiel. "Mesa" ist einfach das Gegenteil von "Meta", also so etwas wie "eine Ebene tiefer". Die Idee ist, dass ein Trainingsprozess (in diesem Kontext normalerweise als *Basis-Optimierer* bezeichnet) potenziell Programme trainieren/finden könnte, die selbst Optimierer sind (der *Mesa-Optimierer*). In der Theorie ist das plausibel: Ein Agent, der aktiv für ein Trainingsziel optimiert, hat eine gute Chance, einer der besten Agenten zu sein, wenn es darum geht, das genannte Trainingsziel tatsächlich zu erreichen. Während Nicht-Optimierer-Agenten wahrscheinlich im Vergleich schlechter abschneiden.

Der Trainingsprozess ist jedoch keine allwissende oder allmächtige Entität, die einfach das bestmögliche Programm oder den besten Agenten findet. Es handelt sich immer noch um einen relativ einfachen Prozess, der normalerweise mit einer zufälligen Initialisierung der Modellgewichte beginnt und dann einen eher stumpfen Suchprozess (wie SGD) durchführt, der die Modellgewichte iterativ verbessert. Es ist unklar, unter welchen Umständen genau ein solcher Prozess tatsächlich eine Konstellation von Modellgewichten *finden* würde, die für eine gegebene Initialisierung einen Mesa-Optimierer hervorbringt.

Dennoch gibt es trotz dieser Unsicherheiten mindestens zwei Gründe, diese Idee sehr ernst zu nehmen:

1. Selbst wenn derzeitige Trainingsprozesse meist keine Mesa-Optimierer hervorbringen und vielleicht sogar die Fähigkeit fehlt, solche Programme im riesigen hochdimensionalen Suchraum der Modellgewichte zu identifizieren, müssen wir nur eine Ebene höher schauen: Hinter jedem Machine Learning Trainingsprozess steht eine Gruppe von **menschlichen Forschern**, die ständig das Trainingsregime anpassen, um die leistungsfähigsten Modelle zu entwickeln. Diese Menschen **haben einen Anreiz, den Trainingsprozess so lange anzupassen, bis er schließlich in der Lage sein wird, Mesa-Optimierer zu erschaffen**.
2. **Menschen könnten als beispielhaft für Mesa-Optimierung betrachtet werden**: Ein einfacher äußerer Prozess, nämlich die Evolution, hat eine Optimierung an Lebewesen durchgeführt, die nach genetischer Fitness selektiert, und hat schließlich (ziemlich fehlgeleitet, aus der Sicht der Evolution) Optimierer in Form von Menschen hervorgebracht.

Ein Vorbehalt bei alldem ist, dass das Konzept eines "Optimierers" schwer sauber zu definieren ist. Und obwohl es leicht ist, Optimierer-Sein als eine binäre Eigenschaft zu betrachten, ist es wahrscheinlich kontinuierlicher. Mit einigen KIs, die mehr  "optimierer-artig" sind, und anderen KIs, bei denen es weniger der Fall ist. Betrachtet man das oben erwähnte Beispiel des Menschen, ist nicht vollkommen klar, wo auf diesem Optimiererkontinuum die meisten Menschen einzuordnen wären. Einige Individuen optimieren ihre Ziele viel mehr als andere, aber praktisch alle Menschen investieren wenigstens einige Anstrengungen, um die Welt um sie herum gemäß ihrer Präferenzen zu verändern. Während also viele Menschen optimiererähnliches Verhalten zeigen, sind wir sicher noch ein Stück entfernt von *perfekten* Optimierern. Aber was auch immer für Menschen zutreffen mag, es ist leicht zu erkennen, dass, wenn wir am Ende einige sehr fähige Mesa-Optimierer-KIs haben, die nicht komplett auf unsere Zielen ausgerichtet sind, dies zu sehr unerwünschten Ergebnissen führen kann.

# Fortgeschritten

- Risks from Learned Optimization: https://www.alignmentforum.org/posts/FkgsxrGf3QxhfLWHG/risks-from-learned-optimization-introduction
- Ein Video von Robert Miles über Mesa-Optimierer: https://www.youtube.com/watch?v=bJLcIBixGj8 
- Mesa optimization: what it is, and why we should care: https://www.lesswrong.com/posts/XWPJfgBymBbL3jdFd/an-58-mesa-optimization-what-it-is-and-why-we-should-care 