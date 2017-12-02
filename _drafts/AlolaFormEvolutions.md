---
title: Alolan Form Evolutions
inline_title: true
---

Alolan forms are one of the headline features of Generation 7 (Sun & Moon). They're new variants of existing Pokémon that take a fresh look at those Pokémon designs. In the fiction of the games, the Alolan forms of existing Pokémon are caused by them migrating to Alola (the region in which Sun & Moon are set) from other regions, and their physiology changing in adaptation to the new environment there. In practice, Game Freak have created a bunch of new twists on existing Generation 1 (Red & Blue) Pokémon - many of them classics that longtime players will remember.

There are many [full lists of Alolan Pokémon](https://www.serebii.net/sunmoon/alolaforms.shtml) online, if you'd like to see all of them. One of the important features of Alolan Pokémon is that they are notably of the same species as the non-Alolan variants. So they can still breed with the non-Alolan variant of their same species from another region.

| Vulpix | Alolan Vulpix |
:-------:|:--------------:
| ![](/assets/img/vulpix.png){:style="max-height:200px;"} | ![](/assets/img/alolan-vulpix.png){:style="max-height:200px;"} |

The classic [Vulpix](https://www.serebii.net/pokedex-sm/037.shtml), on the left, is a fire type and the new Alolan variant, on the right, is an Ice type.

When working to support Sun & Moon in [PokémonCompDB](/pokemoncompdb.html), I had to make sure that my database of Pokémon data only allowed Pokémon to learn moves that they could learn in the games. Though variant forms were something I'd encountered before (on the likes of [Deoxys](https://www.serebii.net/pokedex-sm/386.shtml), [Tornadus](https://www.serebii.net/pokedex-sm/641.shtml), [Giratina](https://www.serebii.net/pokedex-sm/487.shtml), and others) the persistent nature of Alolan forms created some new edge cases.

| Normal | Attack | Defense | Speed |
:-------:|:------:|:-------:|:------:
| ![](/assets/img/deoxys-normal.png){:style="max-height:200px;"} | ![](/assets/img/deoxys-attack.png){:style="max-height:200px;"} | ![](/assets/img/deoxys-defense.png){:style="max-height:200px;"} | ![](/assets/img/deoxys-speed.png){:style="max-height:200px;"} |

Above are the four different forms of Deoxys, which the player can switch between at will by visiting a corresponding meteorite in every game since Generation 4 (Diamond & Pearl).

Pokémon can learn moves in many ways and one of those ways is called "egg moves". This is when a Pokémon knows that move immediately upon hatching from its egg if one of its parents knew that move. Which moves each Pokémon can learn as an egg move vary between each Pokémon species and often egg moves are the only way some Pokémon learn key useful moves.

![](/assets/img/egg.png)
*In the core games, **almost** all eggs look the same*

As I mentioned above, Alolan form Pokémon can breed with their non-Alolan counterparts. But due to differences in design and typing, Game Freak haven't kept the egg move learnset the same across the Alolan and non-Alolan variants. Non-Alolan Vulpix can learn [Feint Attack](https://www.serebii.net/attackdex-sm/feintattack.shtml) as an egg move, while Alolan Vulpix cannot. Alolan Vulpix can learn [Freeze-Dry](https://www.serebii.net/attackdex-sm/freeze-dry.shtml) as an egg move, but non-Alolan Vulpix cannot.

Generally this does make sense - having the ice type Alolan Vulpix learn new and different moves from its fire-type predecessor helps differentiate them and make the Alolan form feel new. Since forms had never persisted across breeding before (and many Pokémon that have variant forms are Legendary and therefore can't breed), this was the first time I'd ever run into a species that had divergent egg moves in its different forms.

![](/assets/img/dugtrios.png){:style="max-height:200px;"}
*Some Alolan form differences are... striking*

But as if that wasn't enough, there's also the concept of pre-evolution only moves. This is where a more evolved Pokémon *does not* learn moves that its less evolved species *do*. This concept has been around since all the way back in Generation 1 (Red & Blue). It's used most often in the following situations:

* When a Pokémon evolves using an evolutionary stone, such as [Growlithe](https://www.serebii.net/pokedex-sm/058.shtml) into [Arcanine](https://www.serebii.net/pokedex-sm/059.shtml) with a [Fire Stone](https://www.serebii.net/itemdex/firestone.shtml)
* When a Pokémon evolves through trading, such as [Haunter](https://www.serebii.net/pokedex-sm/093.shtml) into [Gengar](https://www.serebii.net/pokedex-sm/094.shtml) (and some other variants covered in more depth in [my last post]({% post_url 2017-11-25-CatchingPolitoed %}))
* When Game Freak feel like it

In both of the first two situations, the most evolved Pokémon (the one that you get from using the stone or trading: Arcanine and Gengar in the above cases) mostly stop learning new moves by levelling up. For example, Arcanine's only move that it learns by level up in Sun & Moon is [Extreme Speed](https://www.serebii.net/attackdex-sm/extremespeed.shtml) at level 34. Growlithe, on the other hand, learns a whole swath of moves while levelling up, between [Ember](https://www.serebii.net/attackdex-sm/ember.shtml) at 6 and [Flare Blitz](https://www.serebii.net/attackdex-sm/flareblitz.shtml) at level 45.

This is generally done to prevent players from immediately using the evolutionary mechanic and suddenly having a powerful fully-evolved Pokémon early on in the game. If they do so, that Pokémon will fail to learn its full set of moves as it levels up, and will therefore be weaker in the endgame.

![](/assets/img/arcanine.png){:style="max-height: 300px;"}
*Arcanine is awesome, so I'll understand if you evolve your Growlithe straight away*

In the third case, sometimes Game Freak have pre-evolution only moves seemingly just for fun. [Bulbasaur](https://www.serebii.net/pokedex-sm/001.shtml), for example, learns [Seed Bomb](https://www.serebii.net/attackdex-sm/seedbomb.shtml) at level 37 in Sun & Moon. Neither [Ivysaur](https://www.serebii.net/pokedex-sm/002.shtml) nor [Venusaur](https://www.serebii.net/pokedex-sm/003.shtml) learn Seed Bomb, despite Bulbasaur evolving into Ivysaur at level 16, and Ivysaur into Venusaur at level 32. That means if you want a Venusaur with Seed Bomb (which is quite useful for a physical attacker like Venusaur), you need to prevent your Bulbasaur from evolving (by pressing B on the evolution screen) every. single. level. from 16 to 37.

Saying it's just for fun is a little unfair. From a conceptual point of view, Bulbsaur is the only one of the three that has a seed bulb on its back (it sprouts into a flower when it evolves). So the concept of "Seed Bomb" maps well to it, which you can see here:

| Bulbasaur | Ivysaur | Venusaur |
:----------:|:-------:|:---------:
| ![](/assets/img/bulbasaur.png){:style="max-height:200px;"} | ![](/assets/img/ivysaur.png){:style="max-height:200px;"} | ![](/assets/img/venusaur.png){:style="max-height:200px;"} |


One of the Alolan Pokémon I called out above is Vulpix, who evolves into [Ninetales](https://www.serebii.net/pokedex-sm/038.shtml) via Fire Stone. This falls into the first category I mentioned above of evolutionary stones. So Ninetales has a bunch of moves that it only learns before it evolves from Vulpix. The thing that caught me out here was that (obviously, from a human perspective) only Alolan Vulpix evolves into Alolan Ninetales. So moves learned only by non-Alolan Vulpix are *not* pre-evolution only moves for Alolan Ninetales.

I adjusted my database generation system accordingly to only look for Pokémon of the same form when searching for pre-evolution only moves. Alolan Ninetales would only consider Alolan Vulpix, Alolan [Sandslash](https://www.serebii.net/pokedex-sm/028.shtml) would only consider Alolan [Sandshrew](https://www.serebii.net/pokedex-sm/027.shtml), and so on.

![](/assets/img/alolan-sandshrew.png){:style="max-height:200px;"}
*Look at him! It's like he has a tiny little coat on!*

Promptly, [Exeggutor](https://www.serebii.net/pokedex-sm/103.shtml), [Marowak](https://www.serebii.net/pokedex-sm/105.shtml), and [Raichu](https://www.serebii.net/pokedex-sm/026.shtml) were broken. Why? Because these three Pokémon's pre-evolutions ([Exeggcute](https://www.serebii.net/pokedex-sm/102.shtml), [Cubone](https://www.serebii.net/pokedex-sm/104.shtml), and [Pikachu](https://www.serebii.net/pokedex-sm/025.shtml) respectively) *don't have Alolan forms*. The non-Alolan variants of those Pokémon evolve into the Alolan variants all the time in Sun & Moon. Non-Alolan Exeggutor, Marowak, and Raichu are actually inaccessible in Generation 7, the only way to have them is to import them from a previous game.

| Alolan Exeggutor | Alolan Marowak | Alolan Raichu |
:----------:|:-------:|:---------:
| ![](/assets/img/alolan-exeggutor.png){:style="max-height:200px;"} | ![](/assets/img/alolan-marowak.png){:style="max-height:200px;"} | ![](/assets/img/alolan-raichu.png){:style="max-height:200px;"} |

Again the database generator changed, this time using searching for pre-evolution moves on the same form variant of the pre-evolved species *only if* that species actually *had* a corresponding form. And *then* it worked.

![](/assets/img/whos-that-exeggutor.jpg){:style="max-height:200px;"}
*Game Freak was trolling all of us with Alolan forms, one way or another*