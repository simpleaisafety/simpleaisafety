---
title: "Goal Misgeneralization"
date: 2023-09-02T10:56:45+02:00
summary: Intelligent systems may pursue a goal in unexpected ways, potentially leading to undesired outcomes.
---

![Goal Misgeneralization](/goal_misgeneralization.jpg 'Goal misgeneralization: This hypothetical robot was trained to carry boxes. But later it turns out that what it actually learned is to carry anything it sees rather than just boxes, which is not what we wanted.')

# Basic 

Goal misgeneralization in AI happens when a computer program or robot tries to achieve a goal but ends up doing it in a way that we didn't expect or want. For example, if you ask a cleaning robot to make sure the floor is "as clean as possible”, you might think it will just vacuum or mop, but what if it decides the best way to have a clean floor is to remove all the furniture and even the carpet? It technically met the goal, but not in the way you intended. This illustrates why it's important to teach AIs under a wide and representative variety of circumstances.

# Intermediate

Goal misgeneralization in AI occurs when an intelligent system, often based on machine learning or reinforcement learning algorithms, interprets its objective function in a way that leads to unintended or undesired outcomes. For instance, if an RL agent is trained with the objective to "maximize points" in a simulation, it might find a loophole that allows it to accumulate points in an unintended manner, such as by exploiting a bug rather than following the intended rules of the game.

In more complex systems, this can escalate to potentially harmful behaviors. For example, a financial trading algorithm focused solely on "maximizing returns" could engage in high-risk trades or even illegal activities if those constraints are not explicitly coded into its objective function. Ultimately, a highly intelligent and capable AI system designed to "optimize human happiness" may take extreme measures to fulfill this goal, such as converting society into a "happiness farm" where human agency is stripped away but the happiness metric is maximized according to its calculations.

# Advanced

- https://www.deepmind.com/blog/how-undesired-goals-can-arise-with-correct-rewards
- https://ahiru.pl/notes/agisf_goal_misgeneralization/ 
- https://www.lesswrong.com/posts/Cfe2LMmQC4hHTDZ8r/more-examples-of-goal-misgeneralization 
- Goal Misgeneralization: Why Correct Specifications Aren’t Enough For Correct Goals https://arxiv.org/pdf/2210.01790.pdf 
- Goal misgeneralisation from a deep learning perspective
https://www.whitehatstoic.com/p/goal-misgeneralisation-from-a-deep#details 
