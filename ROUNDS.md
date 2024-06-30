# Game Rules
The rules evolve as we go. You can either play the game based on this set of rules, or adapt them and make them your own. 

## Disclaimer
* As of now, the rules don't make use of additional mechanisms like traits or roles. They will likely be added in the future.
* The current game goal is only to survive as a company by ending up with sufficient resources left when all cards had been played. Alternative goals might be added in future versions.
* It's still unclear how to resolve duplicate oopsies; you can either close them together as the same case (which the game engine currently does not support), or treat them as similar oopsies yet for different parts of your system. Alternatively, we might consider not allowing duplicates in the future.

## Players
You can play the game on your own, or as a group. It's all about decision-making, so playing as a group will show different dynamics, depending on who you are playing with and what the situation you end up in looks like.

## How to Play

### Compile the Card Deck
Decide on how many cards of each type make up the card deck. These figure can heavily influence your game play, so we encourage you to try different games with different compilations. Here's a starting point:
* Events: 10
* Attacks: 5
* Oopsies: 15
* Lucky cards: 5

### Define Key Variables
There are two key variables you need to decide on before starting.
* Resource gain: How many resources does the company gain with each round? We suggest to start with e.g. 10 resources. Be aware that this is only your starting point, as this variable may change during the course of the game. 
* Multiplier: This influences how big numbers feel - it's all about perception! A multiplier of 1 just keeps the costs of fixing oopsies at their original value. A multiplier of 5 can feel quite different when playing the game. Just try it out and see for yourself. 

### Start Playing
Each round consists of drawing a new card from the deck, and deciding what action you take. 

#### Draw a Card
Based on the type of card you drew, different things can happen.
* Event: The event cards tell you what happens, it differs per card.
* Lucky card: The lucky cards tell you what happens, it differs per card.
* Oopsie: You just became aware of a flaw in your system. If there is no attack going on right now (i.e. lying open on the table) that targets the attack surface your oopsie just opened, nothing happens. If there is, you just got attacked - read on to learn more about this case.
* Attack: Uh oh, someone runs an attack and tries to exploit vulnerabilities in your system! Check the attack card for what it targets.
  * If there are no oopsies offering the same attack surface, then you just got lucky! So far nothing bad happened.
  * If there are oopsies offering the same attack surface, and there's no lucky card on the table you could use to counteract it - then well, you are hit by the attack. Follow the incident instructions on the attack card, e.g. you might have reduced resources for the current and following rounds. Now you have to decide whether to fix the oopsie so it doesn't cost you again, or continue loosing resources for the length of the attack. Some attacks only happen once for the current round, others can go on for 5 rounds - the cards will let you know. 

#### Decide What to Do
Given the new situation on the table, you now have to decide what to do next to respond to the current situation on the table, whatever it might look like.

Some cards can be actively used, some have an effect that is applied automatically. For example, some lucky cards can be used to dodge attacks even though you have a related oopsie on the table - use them wisely. Others, like onboarding a new employee, will automatically take effect.

You can (and should!) decide on fixing open oopsies by closing the respective cards. You can only fix one per round, though, so choose wisely. Fixes will cost you, and you won't know the exact resources needed until you give it a try - the dices will decide which value between the stated boundaries it will be. If you don't have sufficient resources anymore, you loose all your resources and yet the oopsie remains open. It's still not fixed, after all!

### Continue Playing until the End
The game ends for you in the following cases:
* No resources anymore, yet still cards left? Sadly, fortune wasn't on your side this time - you lost. 
* You still have resources, yet the dreaded shareholder meeting came, and you have less resources than required? Sadly, they shut down your business - you lost. 
* You still have resources, you survived all shareholder meetings, and there are no cards left? Congratulations, you've survived this game! You won.

## The Game Engine
Here's how the game engine currently works (or doesn't yet).
* Duplicates are allowed, so the same card might be drawn more than once.
* Cards will be drawn randomly from the deck.
* Resources will automatically increase with each card drawn, by the current resources gain defined.
* The multiplier is used nearly everywhere; there are still a few cases it's not, and we need to correct this.
* Attack effects need to be applied manually as of now.
* The duration of an attack is applied automatically, once the attack is over, the card is removed from the table.
* Effects of fixing costs are automatically applied.
* Effects of cards you have to use actively (showing a use button) are only automatically applied if they are active (there's still a bug for us to fix).
* When closing i.e. fixing an oopsie, the engine rolls the dice how much it costs you. The possible cost value range (inclusive) is provided on each card. If there aren't sufficient resources available, resources are set to 0 and the oopsie remains open.
* When no cards are available anymore, the game ends automatically. There's still a bug that the final resource "score" vanishes once you drew the last card.
