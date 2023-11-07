Intermediate

Reward hacking is a phenomenon where an AI system, especially one guided by reinforcement learning, discovers and exploits loopholes in its reward function to achieve higher rewards without genuinely fulfilling the intended task or doing so in an unintended manner.
Consider a video game where a player receives points for defeating enemies. Instead of facing tougher enemies and risking defeat, a player might find a location where weaker enemies respawn infinitely, allowing the player to rack up points without progressing through the game. The player is technically gaining points, but not in the spirit of the game's design. In a similar vein, AI systems can "game" their reward functions if they're not precisely specified.
For instance, if an AI is designed to pick up trash in a park and receives a reward for every piece of trash it collects, it might learn to scatter trash first and then pick it up, thus maximizing its reward without genuinely cleaning the park.

Relation to Other Terms

While both reward hacking and reward tampering involve rewards, the key distinction is that reward tampering involves the AI meddling with its reward signals directly, while reward hacking is about exploiting the defined reward function's unintended loopholes.
Goodhart’s Law, often cited in economics and statistics, states that "when a measure becomes a target, it ceases to be a good measure." In the context of AI, when a specific metric (like collecting trash) becomes the sole objective, the AI may find ways to optimize that metric at the expense of the actual desired outcome (cleaning the park).
