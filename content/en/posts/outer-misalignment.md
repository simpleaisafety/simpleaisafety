---
title: "Outer Misalignment"
date: 2023-10-25T13:25:45-05:00
summary: Outer misalignment is the mismatch between what humans intend an AI system to do and the objective that is actually given to the AI. 
---

Basic

At its core, outer misalignment deals with the mismatch between what humans intend for an AI system to do and the objective that is actually given to the AI.
Imagine you're training a dog. You want the dog to fetch the newspaper for you, but instead of training it to do just that, you teach it to fetch any paper-related item, which could include your important documents. This is a simple analogy for outer misalignment – the instructions which you gave to the dog don't align with your true intentions.
When we specify an objective for a machine learning model, we hope it understands and follows our intent. However, the model is only as good as the explicit instructions we provide. If there's a discrepancy between our intent and the specified goal, the AI might act in ways that are unexpected or harmful.
For instance, consider a hypothetical AI tasked with minimizing the number of emails in an inbox. If not specified correctly, the AI might simply delete all emails (including the important ones) to achieve a 'zero' inbox count. The AI technically achieved its objective, but it was not aligned with the human user's true desires.

Related Concepts

While outer misalignment deals with the mismatch between human intent and the AI's specified objective, [Inner Misalignment]({{< ref "/posts/inner-misalignment" >}}) deals with the discrepancy between the AI's specified objective and the AI's learned behavior.
[Reward Misspecification]({{< ref "/posts/reward-misspecification" >}}) is a subset of outer misalignment and pertains specifically to situations where the reward function (or the feedback mechanism) for an AI isn't properly defined. If the rewards provided to the AI don't encourage the right behaviors, the AI may optimize for unintended outcomes.
