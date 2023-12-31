---
title: "Fehlgeneralisierung von Zielen"
date: 2023-09-02T10:56:45+02:00
summary: Intelligente System können unbemerkt die falschen Ziele lernen, und sich so außerhalb ihrer Trainings-Umgebung unvorhergesehen verhalten.
---

![Fehlgeneralisierung von Zielen](/goal_misgeneralization.jpg 'Fehlgeneralisierung von Zielen: Dieser hypothetische Roboter wurde darauf trainiert, Kisten zu transportieren. Später stellt sich jedoch heraus, dass er tatsächlich gelernt hat, alles zu transportieren, was er sieht, und nicht nur Kisten – das ist nicht, was wir wollten.')

# Grundlagen

Fehlgeneralisierung von Zielen ("Goal misgeneralization") ist ein Problem, das häufig im Bereich des Reinforcement Learnings auftritt: hier lernt ein KI-Agent implizit anhang von einem Belohnungssystem, welche Handlungen unter welchen Umständen wünschenswert sind, und nähert sich so mehr und mehr dem gewünschten Verhalten an. Von Fehlgeneralisierung der Ziele sprechen wir, wenn sich rausstellt, dass die KI tatsächlich etwas anderes gelernt hat als gewünscht, das in der Trainings-Umgebung gut funktioniert hat, in der Praxis (nach dem Training), wenn die Bedingungen sich ändern, jedoch nicht mehr richtig funktioniert.

Ein Beispiel wäre ein Fabrik-Roboter, der lernt herumliegende Dinge in Regale zu stapeln: falls er in der Trainingsumgebung jeweils nur Situationen vorfindet, in denen lediglich Kisten und Regale vorkommen, kann es passieren, dass er tatsächlich lernt _alles_ in Regale zu räumen. Wenn er nun praktisch eingesetzt wird, beginnt er beliebige Dinge in Regale zu räumen.

# Weiterführend

Fehlgeneralisierung von Zielen in der KI liegt vor, wenn ein intelligentes System, das häufig auf Algorithmen des maschinellen Lernens oder des verstärkenden Lernens basiert, seine Zielfunktion in einer Weise auslegt, die zu unbeabsichtigten oder unerwünschten Ergebnissen führt. Wenn beispielsweise ein RL-Agent mit dem Ziel trainiert wird, in einer Simulation "Punkte zu maximieren", könnte er ein Schlupfloch finden, das es ihm ermöglicht, auf unbeabsichtigte Weise Punkte zu sammeln, indem er beispielsweise einen Fehler ausnutzt, anstatt die vorgesehenen Spielregeln zu befolgen.

In komplexeren Systemen kann dies zu potenziell schädlichen Verhaltensweisen führen. So könnte beispielsweise ein Algorithmus für den Finanzhandel, der sich ausschließlich auf die "Maximierung der Rendite" konzentriert, hochriskante Geschäfte oder sogar illegale Aktivitäten durchführen, wenn diese Einschränkungen nicht ausdrücklich in seiner Zielfunktion kodiert sind. Letztendlich könnte ein hochintelligentes und leistungsfähiges KI-System, das darauf ausgelegt ist, "das menschliche Glück zu optimieren", extreme Maßnahmen ergreifen, um dieses Ziel zu erreichen, wie z. B. die Umwandlung der Gesellschaft in eine "Glücksfarm", in der die menschliche Handlungsfähigkeit ausgeschaltet ist, aber die Glücksmetrik gemäß den Berechnungen des Systems maximiert wird.

# Fortgeschritten

(Links in Englisch)

- https://www.deepmind.com/blog/how-undesired-goals-can-arise-with-correct-rewards
- https://ahiru.pl/notes/agisf_goal_misgeneralization/ 
- https://www.lesswrong.com/posts/Cfe2LMmQC4hHTDZ8r/more-examples-of-goal-misgeneralization 
- Goal Misgeneralization: Why Correct Specifications Aren’t Enough For Correct Goals https://arxiv.org/pdf/2210.01790.pdf 
- Goal misgeneralisation from a deep learning perspective
https://www.whitehatstoic.com/p/goal-misgeneralisation-from-a-deep#details 
