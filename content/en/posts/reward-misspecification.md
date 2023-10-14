---
title: "Reward Misspecification"
date: 2023-10-14T12:41:22+02:00
summary: It's difficult to create a reward function that
  precisely reflects what we want.
---

![Reward Misspecification](/king-midas.png 'Reward misspecification is a failure mode of aligning AI models, caused by the inherent difficulty of cleanly formalizing our intentions. A famous fictional example is King Midas, who wished that everything he touched turned to gold.')

# Basic

It turns out to be difficult to clearly formalize a wish in a way that fully reflects our intentions. A famous fictional example is the story of King Midas, who wished that everything he touched turned to gold. This superficially seems like an effective way to become wealthy, but ended up having some rather unintended side effects, such as turning his loved ones into gold, as well as any food he was about to eat.

While the drawbacks of this particular wish may seem obvious, research in machine learning has shown that similar things happen quite often in practice, because it's surprisingly difficult to anticipate whether a given reward function (that is used to train the AI) actually causes the AI to behave in desirable ways, or may actually lead to entirely unexpected and undesirable behaviours, which reveal that the reward function has some gaps or loopholes.

# Intermediate

Reward misspecification is a failure mode of aligning AI models, due to the inherent difficulty of specifying a reward function (or loss function) that assigns rewards to actions or world states that precisely reflect what we want. These functions are used as guidance to steer the AI to some hopefully beneficial behaviour. This is often problematic however, because it tends to be very difficult to construct such a function that really aligns well with what we *actually* want. This is because our goals and desires have a lot of hidden complexity.

Say we ask somebody to get us a coffee. This sounds simple, but there are actually a lot of implicit constraints. E.g. it may be acceptable for the person (or AI) to spend a bit of money to achieve the goal - but probably not $50. We implicitly hope that this action will take no more than a few minutes. Also it should happen without any significant collateral damage and without leaving the kitchen in a mess. In [The Hidden Complexity of Wishes](https://www.lesswrong.com/posts/4ARaTpNX62uaL86j6/the-hidden-complexity-of-wishes), Eliezer Yudkowsky states that "There is no safe wish smaller than an entire human morality". This basically explains the problem with specifying reward functions: in principle, we have to make all our implicit constraints explicit in order to create a reward function that doesn't lead to undesirable outcomes when plugging it into an optimization process.

While the above example may sound a bit theoretical, there's actually a lot of documented cases where reward misspecification actually caused AIs to behave in unexpected and undesirable ways.

## Relation to Other Terms

Reward misspecification is closely linked to the widely used term of *outer misalignment*, and describes the discrepancy between what we (as creators of an AI) want and the reward (or loss) function we create to reflect that. Its counterpart, *inner misalignment*, is another failure mode of AI alignment, referring to the discrepancy between the reward (or loss) function and what the AI actually learns. In practice, quite often both things happen: our reward function does not perfectly reflect our true intentions, and the AI ends up learning something different from the actual reward function (see Goal Misgeneralization).

There's also the term of specification gaming, which generally describes the process of reinforcement learning agents learning to behave in unexpected ways that yield high rewards. This can be considered both good and bad: it can be good in the sense of the AI finding some previously unknown behaviour that actually achieve the goal (e.g. exploits in video games). But quite often it's rather a bad thing, as the AI identifies loopholes in the way the reward function is designed, and exploits them.

# Advanced

- https://course.aisafetyfundamentals.com/alignment?session=2
- "The Effects of Reward Misspecification": https://arxiv.org/abs/2201.03544
- https://openai.com/research/learning-from-human-preferences
- https://www.deepmind.com/blog/specification-gaming-the-flip-side-of-ai-ingenuity
- Table of many goal misspecification examples: https://docs.google.com/spreadsheets/d/e/2PACX-1vRPiprOaC3HsCf5Tuum8bRfzYUiKLRqJmbOoC-32JorNdfyTiRRsR7Ea5eWtvsWzuxo8bjOxCG84dAg/pubhtml 