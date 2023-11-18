---
title: "Inner Misalignment"
date: 2023-11-18T18:23:52+02:00
summary: Inner misalignment is the mismatch between the objective that is given to the AI, and what the AI actually ends up learning. 
---

![Inner vs Outer Alignment](/inner-outer-alignment.png 'Diagram showing the relationship between "Inner" and "Outer" alignment')

# Basic

Inner misalignment describes the mismatch between the objective an AI is trained on, and what the AI actually learns. Usually we would hope that the two are perfectly aligned, but in practice this is rarely the case.

Imagine we train chess playing AI. We can of course easily determine the winner of any game of chess, so we can use this to train the AI with a perfectly valid training signal (so we can rule out outer misalignment), e.g. via self play. When you train this AI for a while, and then play against it, it might indeed seem as if it learned chess very well. However, sometimes the following happens: by making some really unconventional moves, you move the game "out of distribution" – the board then resembles a state of a kind the AI has never encountered during training. Some AIs will now behave strangely, and make strange moves on their own, rather than game-winning ones.

![A robot playing a strange version of chess](/chess-ai.jpg 'This robot has learned regular chess, but is now confronted with a rather non-standard chess board and setup. Chances are its chess skills will not generalize to these new circumstances, and it will play a rather underwhelming match. This can be seen as a case of inner misalignment: it was trained with a proper training signal, but still ended up learning something less general than we would hope.')

# Intermediate

Inner misalignment arises when there's a divergence between the objective we give an AI system and how the system internally learns to achieve that objective. In essence, the AI might develop strategies or behaviors during its training that don't generalize to achieving the objective in all situations, by misgeneralizing from the provided objectives in the training setting.

A common cause of inner misalignment is a "distribution shift": if the situations the AI learned from during training had some kind of bias or did not fully generally represent all possible situations, then it may be that the AI learned some flawed strategy that only happened to work well in these training settings. When the AI then encounters different circumstances during deployment, it can turn out that it behaves in rather unexpected ways. Often this means that it's not effectively achieving the objective anymore.

For instance, if you train a machine learning model to identify zebras in images, the model might not actually learn to recognize the shape and features of zebras. Instead, if most training images of zebras were taken in the African savannah during daytime, the model might just learn to identify the savannah's grassy background or the specific lighting of those photos as indicators of a zebra's presence. Thus, when presented with a nighttime picture of a zebra or one in a different setting, the model might fail to recognize it.

Inner misalignment can be very hard to avoid, as it's difficult to provide the whole range of possible constellations of input values during training – and even if you manage to do that, there are no guarantees the AI will generalize properly. This problem even arises for AIs in rather simple domains, such as LLMs dealing purely with text: A plain text that is 60 characters long already can take on more possible forms than there are atoms in the universe. It would take a tremendous amount of training data to ensure that the model learns the desired behaviour across this whole distribution. Plus, the training data that we usually use for LLMs – human-written text – is of course strongly biased towards human language, which represents only a miniscule subset of all possible strings of text. Some real world examples of this challenge are the existence of [glitch tokens](https://www.youtube.com/watch?v=WO2X3oZEJOA) and [adversarial prompts](https://www.promptingguide.ai/risks/adversarial).

## Relation to Other Terms

While inner misalignment concerns an AI's learned behavior diverging from its specified objective, [Outer Misalignment]({{< ref "/posts/outer-misalignment" >}}) is about the mismatch between the human's true intentions and the objective given to the AI.

Overfitting is a related phenomenon where an AI model becomes too specialized in the training data, potentially performing poorly on new, unseen data. Though overfitting can be one cause of inner misalignment (the model "cheats" by memorizing features specific only to the training data), not all cases of inner misalignment are due to overfitting.

# Advanced
- https://www.alignmentforum.org/tag/inner-alignment
- https://www.lesswrong.com/posts/poyshiMEhJsAuifKt/outer-vs-inner-misalignment-three-framings-1
- https://www.lesswrong.com/posts/pL56xPoniLvtMDQ4J/the-inner-alignment-problem
- Black Box Adversarial Prompting for Foundation Models: https://arxiv.org/abs/2302.04237
- Robert Miles on glitch tokens: https://www.youtube.com/watch?v=WO2X3oZEJOA