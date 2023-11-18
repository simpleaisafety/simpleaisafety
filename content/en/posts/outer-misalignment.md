---
title: "Outer Misalignment"
date: 2023-10-25T13:25:45-05:00
summary: Outer misalignment is the mismatch between what humans intend an AI system to do and the objective that is actually given to the AI. 
---

![Inner vs Outer Alignment](/inner-outer-alignment.png 'Diagram showing the relationship between "Inner" and "Outer" alignment')

# Basic

Outer misalignment deals with the mismatch between what humans intend for an AI system to do and the objective that is actually given to the AI.

Imagine you're training a dog. You want the dog to fetch the newspaper for you, but because you currently have no newspaper at hand, you just pick some random pieces of paper and use them for training. The dog now actually learns not to fetch a newspaper, but any piece of paper – possibly including important documents. That was not your intent, but the way you set up the training process it was actually "correct" for the dog to learn what it learned. This is a simple analogy for outer misalignment – the instructions which you gave to the dog don't align with your true intentions.


When we specify an objective for a machine learning model, we hope it understands and follows our intent. However, the model can only be as good as the explicit instructions we provide. If there's a discrepancy between our actual intent and the specified goal, the AI might end up acting in ways that are unexpected or harmful, even though (or maybe because) it does just what is was taught.
For instance, consider a hypothetical AI tasked with minimizing the number of emails in an inbox. If not specified correctly, the AI might simply delete all emails (including the important ones) to achieve a 'zero' inbox count. The AI technically achieved its objective, but it was not aligned with the human user's true desires.

![A dog carrying a famous painting](/misaligned-dog.jpg 'A very misaligned dog, who learned not to carry newspapers, but anything resembling paper.')

# Intermediate

Training AIs is a complex process, and there's many ways in which it can go wrong. One conceptual model some people find helpful is to differentiate between inner and outer misalignment. The idea behind this is that there are two typical ways in which an AI can learn something that does not align with our intentions: either we did a bad job setting up its training process (e.g. due to reward misspecification), or the AI ended up internalizing a goal or behaviour different from what it was supposed to learn (e.g. due to goal misgeneralization). The former would be outer misalignment.

While the terms of inner and outer misalignment are used frequently in AI Safety discussions and writings, it's noteworthy that some people question the usefulness of the concept. In real world examples, the distinction between what counts as "outer" and what as "inner" is often not perfectly clear, leading to confusion. Still, the distinction helps building intuition for the difficulty of AI alignment: not only do you have to make really sure you encode the right training signal or goal function, you also have to worry about whether the AI will actually learn the thing it is being taught. So while we maybe shouldn't treat inner and outer misalignment as a dichotomy, it still makes sense to appreciate that the diffiulty of alignment exists on multiple levels, and different interventions or research directions may affect inner and outer misalignment risks to different degrees.

## Related Concepts

While outer misalignment deals with the mismatch between human intent and the AI's *specified* objective, [Inner Misalignment]({{< ref "/posts/inner-misalignment" >}}) deals with the discrepancy between the AI's specified objective and the AI's learned behavior.

Outer aligment relates strongly to [Reward Misspecification]({{< ref "/posts/reward-misspecification" >}}), which describes situations where the reward function (or the feedback mechanism) for an AI isn't properly defined. If the rewards provided to the AI don't encourage the right behaviors, the AI may optimize for unintended outcomes.

# Advanced

- https://www.lesswrong.com/tag/outer-alignment 
- https://www.lesswrong.com/posts/JKwrDwsaRiSxTv9ur/categorizing-failures-as-outer-or-inner-misalignment-is 
- https://humancompatible.ai/news/2023/01/03/inner-and-outer-alignment-decompose-one-hard-problem-into-two-extremely-hard-problems/ 
- https://www.lesswrong.com/posts/xMQ7vwFACQX3gZouv/reframing-inner-alignment 
