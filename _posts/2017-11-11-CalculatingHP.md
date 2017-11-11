---
title: Calculating a Pokémon's HP
inline_title: true
---

How much HP should this Pokémon have? That depends on a lot of factors. At some level, like all other stats, the Pokémon will have a Base HP. Different species ([Bulbasaur](https://www.serebii.net/pokedex-sm/001.shtml) vs [Arceus](https://www.serebii.net/pokedex-sm/493.shtml) vs [Umbreon](https://www.serebii.net/pokedex-sm/197.shtml), and all other 799 of them) have differing Base HPs. Pokémon gain HP as they level up, so a level 76 [Chansey](https://www.serebii.net/pokedex-sm/113.shtml) will have a lot more HP than a level 5 one.

Each individual Pokémon you catch will have different HP IVs - the initial seed of how much better or worse its HP will be than other Pokémon of the same species. (Not all Rattata are made the same.) And each Pokémon you train will accrue some EVs - and HP EVs will increase their HP. A Pokémon's maximum HP, unlike the other stats (Attack, Defense, Special Attack, Special Defense, and Speed) cannot be modified mid-battle.

As of Generation 3 (Ruby, Sapphire, & Emerald), the formula for calculating the HP of an individual Pokémon is:

![](/assets/img/hp-stat-calculation.png)
*Pokémon involves more math than you might expect*

⌊⌋ represent a "floor" function, meaning round the expression inside down to the nearest whole integer. (4.1, 4.5, and 4.9 would all become 4, for example.) The image of this formula is from [Bulbapedia](https://bulbapedia.bulbagarden.net/wiki/Statistic).

Base means the Pokémon's Base HP stat. IV is how many IVs it has in HP (from 0 to 31). EV is how many HP EVs it has earned (between 0 and 252). And Level is your Pokémon's level (from 1 to 100).

So that tells you how to calculate a given Pokémon's HP exactly. Or your Pokémon could be a [Shedinja](https://www.serebii.net/pokedex-sm/292.shtml), in which case it has a HP of 1. 

Shedinja is the only Pokémon that doesn't follow the formula for **any** of their stats. 802 Pokémon and Game Freak have elected to do this *once*. Which means [PokémonCompDB](/pokemoncompdb.html) needs to support the general case of fixed stats (or at least fixed HP).

![](/assets/img/shedinja.png){:height="200px"}
*Look at it. **Look at it!***

The fixed HP stat does add a lot to Shedinja's overall design. Shedinja's [Wonder Guard](https://www.serebii.net/abilitydex/wonderguard.shtml) ability makes the Bug/Ghost Pokémon immune to all damage that isn't super effective. So the idea is that Shedinja can't be beaten *unless* you have a super effective move available, in which case Shedinja is beaten immediately. (Because Shedinja is Bug/Ghost, the attack needs to be either Fire, Flying, Rock, Ghost, or Dark.)

Given that Shedinja was added in Generation 3 (a whole 14+ years ago), I'm surprised this kind of ability and fixed stat mechanic haven't resurfaced since then.

And that's today's edge case, the *only* Pokémon that doesn't listen to the HP formula.