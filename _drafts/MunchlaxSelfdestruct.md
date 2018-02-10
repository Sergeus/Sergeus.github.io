---
title: Teaching Munchlax Self-destruct
inline_title: true
---

This is it, folks. This is the Pokémon peculiarity that inspired this blog in the first place. Today, I'm going to talk about how you can obtain a Munchlax that knows Self-destruct and how this particular move tripped up PokémonCompDB when I first encountered it. Last week I mentioned that some of the edge cases I've discovered mean things are particularly difficult for the player to do and others are challenging for PokémonCompDB from a data perspective. This one was both.

So who are the players in this elaborate game? Munchlax, its evolved form Snorlax, and the move Self-destruct. Snorlax is a classic Pokémon I'm sure many of you recognize from all the way back in Generation 1 (Red & Blue). Its laziness and penchant for sleeping all the time is well known:

// image

Munchlax is the baby version of Snorlax, introduced as a pre-evolutionary form to Snorlax in Generation 4 (Diamond & Pearl). Like Snorlax, Munchlax is known for eating a lot of food, though it's not usually characterized as being quite as lazy:

// image

Self-destruct is a classic Pokémon move, introduced in Generation 1. The user of the move explodes, doing a lot of damage to its opponent(s) (and ally if it has one), unless, since it's a Normal type move, the targets are Ghost Pokémon, which will take no damage. Then, the user of Self-destruct faints. All fairly self-explanatory. There's even a souped up version of Self-destruct called Explosion, also introduced in Generation 1, but Munchlax and Snorlax can't learn that one.

Why is Self-destruct on Munchlax so special? Munchlax, in every game since it has been introduced, has been able to learn Self-destruct as an egg move. I've talked about egg moves before, where a newly hatched Pokémon can emerge from its egg knowing that move if one of its parents knows it.

Like most other baby Pokémon (such as Cleffa, Magby, and others), breeding a Snorlax to get a Munchlax isn't just a case of putting Snorlax in the daycare like most others. Presumably since it used to be possible to hatch Snorlax out of an egg, Game Freak wanted to keep that consistent. So by default you'll just get a level 1 Snorlax. But if the Snorlax is holding a Full Incense (not a Lax Incense, which I keep forgetting) then Munchlax will hatch out of the egg instead of Snorlax.

// image

When PokémonCompDB is processing egg moves, it explores how each of the possible parents that can know that move learn it. I've mentioned in the depths of the PokémonCompDB page that the application's database is built up by parsing fan websites that list this data, mostly Serebii. I first encountered an issue with Munchlax when trying to parse which Pokémon could be a parent to teach it Self-destruct. PokémonCompDB wasn't finding any parents. I've learned from working on this application for a while that my first response should always be to just look at the web page I'm trying to parse, because some problems are usually quite obvious to a human eye:

// image of empty egg parent list for munchlax

Well, there's your problem. No parents listed means no parents can be found. So I dug manually - why is the above blank? Well, it's blank because the parent for Munchlax that can know Self-destruct is Snorlax, but the way it learns it doesn't fall into any of those categories.

Snorlax can learn Self-destruct one way: from the move tutor in Pokémon XD: Gale of Darkness on the GameCube.

// image

There are *a lot* of games between Pokémon XD and Pokémon Ultra Sun & Ultra Moon. There is a lot of *hardware* between those two games. Gale of Darkness came out in 2005, Ultra Sun & Ultra Moon at the end of last year, 2017. And yet, Ultra Sun & Ultra Moon still have that entry in Munchlax's egg move table to allow Self-destruct to be passed down from that one game twelve years ago where Snorlax could learn it. Did I mention that the move tutor in Pokémon XD, unlike its newer counterparts in later generations, can *only teach each move once*? So you can only teach Self-destruct to *one* Pokémon that way in each save you have in Pokémon XD.

The process of getting from XD to Ultra Moon involves a GameCube (or Wii), the GameBoy Advance to GameCube link cable, a copy of Pokémon XD, a GameBoy Advance (not a DS with a GBA slot - the link cable only fits into the GBA itself), a Generation 3 game (Ruby, Sapphire, Emerald, Fire Red, or Leaf Green), a Generation 4 game (Diamond, Pearl, Platinum, Heart Gold, or Soul Silver), a DS with a GBA slot (so either the original DS phat or DS Lite), a Generation 5 game (Black, White, Black 2, or White 2), a 3DS, and a copy of Pokémon Ultra Moon. Nintendo stopped making a significant amount of that hardware years ago.

But you know what? From years of being a Pokémon fanatic, I actually have all of that stuff. So next week, I'm going to take you through obtaining the elusive Munchlax with Self-destruct!