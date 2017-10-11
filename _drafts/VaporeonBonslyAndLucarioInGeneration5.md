---
title: Import Level Up Moves from Generation V
---

Starting as I mean to continue, my first post has a fun little anecdote about why some Pokémon that you might not expect are unique in interesting and parser-defying ways.

While developing [PokémonCompDB](/Pokémoncompdb.html), I needed to bundle up all of the data about how all of the different Pokémon learn their moves into a database for the application to use. This meant that I had to come up with common patterns between how these moves were learned.

Some patterns are fairly obvious. Many Pokémon learn a given move at a certain level. [Pikachu](https://www.serebii.net/pokedex-sm/025.shtml) learns Thunder Wave at level 18, for example. There is a bit of a wrinkle when this tends to vary by game. Pikachu learns Thunder Wave at level 18 *now*, in Pokémon Sun & Moon. But [back in Pokémon X & Y](https://www.serebii.net/pokedex-xy/025.shtml), Pikachu learned Thunder Wave at level 13.

![](/assets/img/pikachu-thunder-wave.png)
*Let's pretend it was a Pikachu that used Thunder Wave on this Meditite*

All fine, that's generally a pattern that I can deal with. When I was developing the application first, the only games I was really concerning myself with were Omega Ruby & Alpha Sapphire - the most recent games at the time in 2016.

But Pokémon, since the original Ruby & Sapphire back in 2003, has an importing mechanism for bringing all of your monsters over from the older games into the next [generation](https://bulbapedia.bulbagarden.net/wiki/Generation). This is where a lot of fun complexity creeps in. Often there are ways of obtaining moves on certain Pokémon in older games that are no longer available. Pikachu can learn Mega Punch in Fire Red & Leaf Green (back in Generation 3), but not any later games, for example. In those cases, I need to still be able to represent those moves, but flag up to the user that they'll need to import their Pokémon from an older game if they want to use that move.

Omega Ruby & Alpha Sapphire are a part of Generation 6 of Pokémon, along with X & Y. This meant that Generation 5, made up of Black & White and Black 2 & White 2, was a frequently referenced previous generation. And since I was working on a database for Generation 6, the only moves that mattered from Generation 5 were the ones that specific Pokémon could no longer learn in the latest games. That reduces the number of moves involved a lot (especially because there is a big crossover between the move tutors available in Omega Ruby & Alpha Sapphire and the ones in Black 2 & White 2).

![](/assets/img/pokemon-bank-logo.jpg)
*Pokémon Bank, the 3DS application, was how you imported from Generation 5 to 6*

Looking at a few sample Pokémon that learned moves in Generation 5 and no longer learned those moves in Generation 6, I foolishly assumed that all of the levels these Pokémon learned these moves were consistent across all of Generation 5. So any move that they learned at level 5 in Pokémon Black, they would learn at the same level in Pokémon Black 2.

Out of 494 Pokémon available in Generation 5, there are three exceptions to that rule:

Bonsly                                       | Lucario                                       | Vaporeon
:-------------------------------------------:|:---------------------------------------------:|:----------------------------------------------:
![](/assets/img/bonsly.png){:height="200px"} | ![](/assets/img/Lucario.png){:height="200px"} | ![](/assets/img/Vaporeon.png){:height="200px"}

These three Pokémon learn moves in Generation 5 that they can't learn in Generation 6. But they *also* don't learn those moves the same way in Black & White as they do in Black 2 and White 2 (all 4 of which are in Generation 5).

Even better, the differences between Black & White and Black 2 & White *aren't even the same for all three*.

If you read the [about page](/about.html), I told you Game Freak's designers are amazing and crazy, and this is exactly the kind of tiny detail that makes me think that.

## Bonsly
Bonsly does not learn Slam in Generation 6. 