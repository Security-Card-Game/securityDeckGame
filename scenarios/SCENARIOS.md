# Scenario cards

Scenario cards can be either selected or drawn at random before the game starts to provide a setting to base decisions on.

The data format is a simple JSON with the structure:

``` json
{
    "title": "Survive as brand-new startup",
    "description": "You've literally just founded your startup and grew to 5 people. There's no money to invest, you first need to earn it. No one knows you yet! Hence, your only goal for now is to keep running.",
    "preset": {
        "resources": 0,
        "reputation": 0,
        "resourceGain": 5,
        "multiplier": 1
    },
    "goal": {
        "minimumResources": 1,
        "minimumReputation": 1
    },
}

{
    "title": "Established, well-loved brand",
    "description": "You've been on the market for a whole while. People really love your product over your competitors' offers, and your whole company is built on that. Keep your reputation up no matter the costs!",
    "preset": {
        "resources": 1000,
        "reputation": 90,
        "resourceGain": 50,
        "multiplier": 10
    },
    "goal": {
        "minimumResources": 100,
        "minimumReputation": 85
    },
}

{
    "title": "Move fast and make profit",
    "description": "Who cares about stability! We need to be faster than our competitors or we're out of the market. If things break or go wrong on that way, so be it. Our goal is to make profit fast!",
    "preset": {
        "resources": 800,
        "reputation": 40,
        "resourceGain": 20,
        "multiplier": 5
    },
    "goal": {
        "minimumResources": 1300,
        "minimumReputation": 20
    },
}

{
    "title": "Sustainable pace",
    "description": "We've been around for a while and care deeply about people - our employees just as well as our customers. We invest carefully and thoughtfully into doing the right thing, while also slowly growing our company in a sustainable way. That's why we want to keep tech debt at bay and evolve our product just based on current needs.",
    "preset": {
        "resources": 300,
        "reputation": 90,
        "resourceGain": 10,
        "multiplier": 3
    },
    "goal": {
        "minimumResources": 350,
        "minimumReputation": 80
    },
}

{
    "title": "Legacy strikes again",
    "description": "Technical debt? Rather close to bankruptcy! We've been long on the market and for a whole while it's been fine not to modernize. Now we're long beyond the point we should have invested and are stuck with a huge legacy system. Everything takes longer and costs more! We're trying to keep alive. Any big security incident would hurt us deeply as we won't be able to fix things in time before people move on to our competitors.",
    "preset": {
        "resources": 600,
        "reputation": 60,
        "resourceGain": 5,
        "multiplier": 10
    },
    "goal": {
        "minimumResources": 500,
        "minimumReputation": 40
    },
}
```