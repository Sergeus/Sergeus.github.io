---
title: Meowstic, the True Nidoran
inline_title: true
---

This week, I'm celebrating Christmas by talking about Meowstic. Exciting, I know! Meowstic is a Pokémon that is significantly different when it's either male or female. I've talked about gender dimorphism in Pokémon before and some of the other fun edge cases I've discovered to do with it. Mostly, Pokémon gender differences (when they exist) are cosmetic, but in Meowstic the differences affect several things: appearance, stats, abilities, and move sets. Each gender of Meowstic is basically a different form (and I've discussed form differences a bit before as well). This isn't the first time something like this has happened in Pokémon, but Meowstic is different from its predecessor, Nidoran, in a few ways that caused me additional headaches.

So, who's this Pokémon I'm talking about? This is Meowstic:

// image of meowstic

Longtime Pokémon players will remember Nidoran from Generation 1 (Red & Blue). More specifically, Nidoran♂ and Nidoran♀. Nidoran♂ evolves into Nidorino and then Nidoking. Nidoran♀ evolves into Nidorina and then Nidoqueen. Back in Generation 1, Pokémon didn't have genders, that was introduced in Generation 2 (Gold & Solver). The design of Nidoran as a Pokémon essentially imitates animal gender dimorphism, in that the males and females mature differently to one another.

With the lack of genders in Generation 1 to facilitate that, Game Freak made Nidoran♀ and Nidoran♂ separate *species* (which means they have different uniquely identifying Pokédex numbers) so that they could have separate stats. Even though genders were added later, the Pokédex number of a Pokémon has never changed in the series, and it seems Game Freak want to retain that. Nidoran has remained split into two species in all of the games since.

That decision from way back in 1995 or so (assuming it was decided the year before Generation 1 was released) actually helped me out quite a bit. By considering them separate species, I had a very similar case to most other Pokémon. Each one had a gender distribution (100% female or male, depending on which one you were referring to) and generally just had their own pools of moves, abilities, and evolutions. While they were related in concept, from a statistical point of view they didn't actually have anything to do with each other and could be treated exactly like every other Pokémon.

// image of Nidorans

Along came Generation 6 (X & Y) and Meowstic. Meowstic follows a similar conceptual design to Nidoran: male and female Meowstic have different abilities, stats, and moves. But the capabilities of the games to represent gender differences have changed since Nidoran was introduced. Male and female Meowstic are *not* separate species. They have the same Pokédex number.

This means that the different forms of Meowstic are effectively its gender. The user switching the gender of their intended set needs to update the appearance of the Meowstic being used. Any moves one has that the other can't learn need to be removed. Of course, their abilities *overlap*: both of them can have the Keen Eye and Infiltrator abilities, and then female Meowstic can have Competitive and male Meowstic can have Prankster. So if the user has chosen one of the overlapping abilities, we need to keep it the same, but if they've chosen one of the exclusive ones and then switches the gender of the Meowstic they want to train, PokémonCompDB needs to automatically choose a different ability, to prevent the user from ending up with an impossible set.

All of this meant plugging gender into the form machinery that I've described before for Rotom and other Pokémon. To this day, there are workarounds when generating a new Pokémon database specifically put in there to deal with Meowstic. Even though Nidoran came first, it was Meowstic that subtly changed the game from all of the other Pokémon.

The one last difference between Meowstic and Nidoran is that, thankfully, Meowstic does not evolve. But Game Freak have added new evolutions to existing Pokémon before. And it wouldn't surprise me if they make this even more complicated for me in a future generation by adding branching evolutions to the Meowstic family. What about evolutions that branch for the first one but then rejoin to the same species at the end, just to be extra confusing?