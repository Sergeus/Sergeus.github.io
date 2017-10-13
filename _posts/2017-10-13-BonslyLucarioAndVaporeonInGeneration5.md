---
title: Vaporeon, Bonsly, and Lucario in Generation 5
---

Starting as I mean to continue, my first post is about how three specific Pokémon learn moves subtly and surprisingly differently from most others in Generation 5 (Pokémon Black & White and Black 2 & White 2). And by most others I mean all of the others in the then-494 total Pokémon.

While developing [PokémonCompDB](/Pokémoncompdb.html), I needed to bundle up all of the data about how all of the different Pokémon learn their moves into a database for the application to use. This meant that I had to come up with common patterns between how these moves were learned.

Some patterns are fairly obvious. Many Pokémon learn a given move at a certain level. [Pikachu](https://www.serebii.net/pokedex-sm/025.shtml) learns Thunder Wave at level 18, for example. There is a bit of a wrinkle when this tends to vary by game. Pikachu learns Thunder Wave at level 18 *now*, in Pokémon Sun & Moon. But [back in Pokémon X & Y](https://www.serebii.net/pokedex-xy/025.shtml), Pikachu learned Thunder Wave at level 13.

![](/assets/img/pikachu-thunder-wave.png)
*Let's pretend it was a Pikachu that used Thunder Wave on this Meditite*

All fine, that's generally a pattern that I can deal with. When I was developing the application first, the only games I was really concerning myself with were Omega Ruby & Alpha Sapphire - the most recent games at the time in 2016.

But Pokémon, since the original Ruby & Sapphire back in 2003, has an importing mechanism for bringing all of your monsters over from the older games into the next [generation](https://bulbapedia.bulbagarden.net/wiki/Generation). This is where a lot of fun complexity creeps in. Often there are ways of obtaining moves on certain Pokémon in older games that are no longer available. Pikachu can learn [Mega Punch](https://www.serebii.net/attackdex/megapunch.shtml) in Fire Red & Leaf Green (back in Generation 3), but not any later games, for example. In those cases, I need to still be able to represent those moves, but flag up to the user that they'll need to import their Pokémon from an older game if they want to use that move.

Omega Ruby & Alpha Sapphire are a part of Generation 6 of Pokémon, along with X & Y. This meant that Generation 5, made up of Black & White and Black 2 & White 2, was a frequently referenced previous generation. And since I was working on a database for Generation 6, the only moves that mattered from Generation 5 were the ones that specific Pokémon could no longer learn in the latest games. That reduces the number of moves involved a lot (especially because there is a big crossover between the [move tutors](https://bulbapedia.bulbagarden.net/wiki/Move_Tutor) available in Omega Ruby & Alpha Sapphire and the ones in Black 2 & White 2).

![](/assets/img/pokemon-bank-logo.jpg)
*Pokémon Bank, the 3DS application, was how you imported from Generation 5 to 6*

Looking at a few sample Pokémon that learned moves in Generation 5 and no longer learned those moves in Generation 6, I foolishly assumed that all of the levels these Pokémon learned these moves were consistent across all of Generation 5. So any move that they learned at level 5 in Pokémon Black, they would learn at the same level in Pokémon Black 2.

Out of 494 Pokémon available in Generation 5, there are three exceptions to that rule:

Bonsly                                       | Lucario                                       | Vaporeon
:-------------------------------------------:|:---------------------------------------------:|:----------------------------------------------:
![](/assets/img/bonsly.png){:height="200px"} | ![](/assets/img/Lucario.png){:height="200px"} | ![](/assets/img/Vaporeon.png){:height="200px"}

These three Pokémon learn moves in Generation 5 that they can't learn in Generation 6. But they *also* don't learn those moves the same way in Black & White as they do in Black 2 & White 2 (all 4 of which are in Generation 5).

Even better, the differences between Black & White and Black 2 & White *aren't even the same for all three*.

If you read the [about page](/about.html), I told you Game Freak's designers are amazing and crazy, and this is exactly the kind of tiny detail that makes me think that.

## [Bonsly](https://www.serebii.net/pokedex-bw/438.shtml)
Bonsly does not learn [Slam](https://www.serebii.net/attackdex-xy/slam.shtml) in Generation 6. Slam is not a particularly noteworthy or powerful move. In fact, its relatively low accuracy often makes it annoying to use.

In Pokémon Black & White, Bonsly learns Slam at level 38. In Pokémon Black 2 & White 2, Bonsly learns Slam at level 15. In fact, most of Bonsly's level up learnset has been modified between Black & White and Black 2 & White 2, but Slam is the only move that Bonsly *doesn't* also learn in Generation 6.

This was the first Pokémon I ran into that had this kind of difference. I then began to wonder why this might be the case. Overall the changes to Bonsly's moves made it easier to train - it learns most moves at lower levels. Obviously, I can only conjecture why these changes were made.

One reason might be that Bonsly wasn't easily available in Black & White: you had to use the [Dream World](https://bulbapedia.bulbagarden.net/wiki/Pok%C3%A9mon_Dream_World) (on the Pokémon website on PC) or transfer it over from an even *older* game (Generation 4 and before). In Black 2 & White 2 you can find Bonsly in the game, but only through the relatively circuitous method of capturing a [Sudowoodo](https://www.serebii.net/pokedex-bw/185.shtml) from a [Swarm](https://www.serebii.net/black2white2/swarms.shtml) (which is only available after you beat the Elite Four and finish the main story) and breed it while it's holding a Rock Incense.

![](/assets/img/sudowoodo.png){:height="200px"}
*Sudowoodo, who Bonsly evolves into*

By that stage of the game, the player seems unlikely to need assistance training a Bonsly. They've finished the game already and have proven they understand the more labyrinthine breeding mechanics.

However, if you look back to the previous games, you may see another clue. Bonsly's level up learnset in Black & White is *the same* as its learnset was back in Generation 4 (Diamond, Pearl, & Platinum and Heart Gold & Soul Silver). It may simply be that since Bonsly wasn't available to be caught in Black & White, Game Freak didn't update its moves. When Bonsly became available in Black 2 & White 2, its learnset was readjusted to be in line with others in Generation 5.

That's my guess for now.

## [Lucario](https://www.serebii.net/pokedex-bw/448.shtml)
Lucario does not learn [Force Palm](https://www.serebii.net/attackdex-bw/forcepalm.shtml) by level up in Generation 6.

Similar to Bonsly, the level at which Lucario learns Force Palm changes between Black & White and Black 2 & White 2. But Lucario (and its pre-evolved form Riolu) haven't had their whole level up learnset changed. In Black & White they learn Force Palm at level 11 and [Feint](https://www.serebii.net/attackdex-bw/feint.shtml) at level 15. In Black 2 & White 2 they learn those moves the other way around.

![](/assets/img/riolu.png){:height="200px"}
*Riolu, who evolves into Lucario*

Like Bonsly, for the two moves that have changed, Lucario and Riolu learn them at the same levels back in Generation 4. But unlike Bonsly, Lucario and Riolu's learnsets *were otherwise changed* moving from Generation 4 to Black & White.

I'm not sure about any reason for this change. Feint is a relatively complicated move to use correctly (it only works against specific moves used by your opponent), so learning it at a lower level seems more confusing in the early game, if anything. I'm sure there's a reason, and it's this kind of mystery that keeps me coming back to trying to figure all of this out.

Oh, and you might be wondering why I called out Lucario in the header of this section, and not Riolu? Since I've said about that Riolu's level up learnset *did* change between Black & White and Black 2 & White 2.

But of course, unlike Lucario who it evolves into, Riolu *does* still learn Force Palm by level up in Generation 6. And Riolu evolves when it levels up while very happy with its trainer (also only during the day) which is all very unlikely to come together before level 15, after which point none of this even matters because *it will already know Force Palm*. So there's that.

## [Vaporeon](https://www.serebii.net/pokedex-bw/134.shtml)
Fans of classic Pokémon will recognize Vaporeon as [Eevee](https://www.serebii.net/pokedex-bw/133.shtml)'s water evolution from all the way back in Generation 1 (Red, Blue, & Yellow).

Vaporeon doesn't learn [Bite](https://www.serebii.net/attackdex-bw/bite.shtml) in Generation 6. Bite is a fairly weak move, but notably changed from a Normal type move to a Dark type move in Generation 2.

In Black & White, Vaporeon learns Bite at level 32. Vaporeon *doesn't learn Bite* in Black 2 & White 2. So not only can the level they learn moves at change, but moves can be dropped altogether as well.

Why might Game Freak have changed this? Bite was Vaporeon's only Dark type move in Black & White (the only one that does damage anyway - it also learns [Fake Tears](https://www.serebii.net/attackdex-bw/faketears.shtml) as an egg move), so it does give it a bit more coverage: super effective attacks against Ghost and Psychic. Though it can already learn [Shadow Ball](https://www.serebii.net/attackdex-bw/shadowball.shtml) (a Ghost type attack) by TM to do super effective damage against Psychic anyway.

The [Water Stone](https://www.serebii.net/itemdex/waterstone.shtml) (which causes Eevee to evolve into Vaporeon) and Eevee itself are available much earlier in Black 2 & White 2 than in Black & White, so it may be a balancing change due to that. Like Bonsly and Lucario, Eevee (and therefore Vaporeon) wasn't available in Black & White without being transferred from an older game or the Dream World.

![](/assets/img/eevee.png){:height="200px"}
*Eevee, the Pokémon that evolves into Vaporeon (and 7 other eons)*

But then, even though Vaporeon no longer learned Bite in Black 2 & White 2, Eevee *does*. At level 29. So if you really want Bite on Vaporeon in Black 2 & White 2, you can just level up Eevee to 29 and *then* evolve. Maybe that's it - a very subtle way of getting players to play with Eevee for a bit longer, instead of immediately evolving it into Vaporeon. I'm sure the other 5 folks in the world besides me who noticed this took their time!

## Wrap Up

And that's all we have for today! I've got a bunch more Pokémon data tidbits, so I'll be back soon with another!