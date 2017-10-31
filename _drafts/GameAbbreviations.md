---
title: Game Abbreviations
inline_title: true
---

Such a simple problem. "Which Pokémon game is this?" You would think that looking at the data for where a Pokémon learned a move, it would be obvious *which game* that move was learned in. Unfortunately, you would be wrong.

When I was initially working on [PokémonCompDB](/pokemoncompdb.html), Omega Ruby & Alpha Sapphire (in Generation 6) were the latest games. I've mentioned before that you can import Pokémon from previous games over to the next generation, starting from the original Ruby & Sapphire. I've also mentioned that for PokémonCompDB to work, I needed to parse a lot of websites to generate the data needed to understand the games. 

For brevity, the Pokémon games are often referred to by an abbreviation. "RSE" is Ruby, Sapphire, & Emerald for example. These abbreviations are mostly established by fan consensus and not often canonical. They helped me out because they were easy to display:

![](/assets/img/game-abbreviation-example.png)
*Omega Ruby, made succinct*

On a lot of the fan sites that I was parsing to generate the data set for PokémonCompDB, these abbreviations were used in place of the names of the game, also for brevity. When working with Omega Ruby & Alpha Sapphire, the following games were available to be imported from:

* Ruby, Sapphire, & Emerald - RSE
* Fire Red & Leaf Green - FRLG
* Diamond, Pearl, & Platinum - DPPt
* Heart Gold & Soul Silver - HGSS
* Black & White - BW
* Black 2 & White 2 - B2W2
* X & Y - XY
* Omega Ruby & Alpha Sapphure - ΩRαS (or ORAS)

I'll trust you to pick apart which bits of the abbreviations refer to which names. Often this meant that when there are divergences between the two games within a generation (like I described in [my post about Bonsly, Lucario and Vaporeon in Generation 5]({% post_url 2017-10-13-BonslyLucarioAndVaporeonInGeneration5 %})), I would need to recognize the individual game's abbreviation in isolation.

Then along came Sun & Moon. Immediately there's a problem: does S mean Sun or Sapphire?

While unexpected, this was resolved easily enough. Sapphire came first - it has "claimed" the abbreviation S. I'll use "Su" for Sun and all will be well. As Sun is the latest game at the moment, any data is implicitly for Sun & Moon, unless it specifies otherwise (like if the site listed that you must import a Pokémon from Diamond & Pearl, then that data is associated with those games).

However, Nintendo did something else unexpected. They re-released Red & Blue and Gold & Silver on the Virtual Console for the 3DS. And they *added* the capability to import from the digital versions of these classic games into Pokémon Bank, and from there into Sun & Moon. Like all other Pokémon games, Generations 1 and 2 provided some unique moves that could be learned by certain Pokémon. UNIQUE MOVE EXAMPLE HERE

Suddenly there are *a lot* more games accessible in Sun & Moon than there were when I worked with Omega Ruby & Alpha Sapphire. And now, the abbreviation problem became a bit more pronounced:

* Does R mean Red or Ruby?
* Does B mean Blue or Black?
* Does Y mean Yellow or Y?
* Does S mean Silver, Sapphire, or Sun?

For my own data, I can change the abbreviations used for each game. I can follow the same logic I did for Sun - letting the older game "claim" the shortest abbreviation. Ruby is "Ru", Black is "Bl", Sapphire is "Sa", and Sun is "Su".

But what do I do with Yellow? Y doesn't have any more letters. In the end I had to assign Yellow the abbreviation "Ye", due to lack of other letters, despite the almost universal acceptance of the abbreviation "RBY" for Red, Blue, & Yellow in Generation 1.

Not to mention, most Pokémon fan sites are designed with human viewers in mind, not automated parsers. There is a lot of information embedded in the context of how you have navigated to where you are. If a move is learned in "Gen I (Y)" that's "obviously" Yellow, not Y. In these cases, I needed the parser to guess at context - it's not enough to just look at the abbreviations used for the games, you also need to know where you're importing your data for. Y will tend to mean different things when used alongside "RB" or "Gen I". "B" means something different next to "R" than "W", etc.

This wasn't a particularly challenging technical problem (choose a set of unique strings), but it was one, like so many others, that I didn't expect to have so many permutations.