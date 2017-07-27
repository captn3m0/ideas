# research-idea-boardgame-ai-gym

The idea is a mix of 2 things: reading research papers about Monopoly, and playing a lot of boardgames. There is a lot of good research work around monopoly [0] and certain card games (Poker etc), but modern board games (Catan has a little research community) haven't been looked at much. I wanted to do simulation-based research for modern games, but found that there is no easy tooling available to do this.

CardWorld is "OpenAI Gym for boardgames". The complete idea is:

1. Have a board game framework in place that allows people to write rulesets for their favorite games. These get registered as environments in the Gym.
2. Allow anyone to submit a agent script for this environment that plays this game. This could be written in any language that the platform supports.
3. Have a runner system that runs these agents against each other.

The benefits I can see are these:

1. Crowdsource AI research on turn-based games. The easier it is to write a bot that plays Hearts, the more people will try their hand at it.
2. Improve our understanding of Card Game Modelling. There has been some research in this area earlier[1] involving languages specific to model this, but I think there is a lot of scope of improvement here.
3. Give the boardgame community the tools to simulate and understand strategies for modern board games. Everyone knows you must buy the Transports in Monopoly, but what is the optimum strategy for Settlers of Catan?
