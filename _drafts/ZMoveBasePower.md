---
title: Z-Move Base Power
inline_title: true
---

[Z-moves](https://bulbapedia.bulbagarden.net/wiki/Z-Move) are one of the new headline features in Generation 7 (Sun & Moon). There are quite a few unique things about them compared to... pretty much every other move that's come before. They can be used only once per battle, to transform one of your Pokémon's existing moves into a more powerful Z-Move. They're unlocked by a special item called a Z-Crystal that the Pokémon must be holding, with one Z-Crystal available per type. <sup>(And a few that are only for specific Pokémon like Pikashunium Z for Pikachu.)</sup> They have hugely different effects based on which normal move you turn into a Z-Move.

Along with a couple of Pokémon-specific Z-Crystals, there is a grand total of one Z-Crystal that can be used by *multiple **specific*** Pokémon: Tapunium Z, which is used by Tapu Koko, Tapu Lele, Tapu Bulu, and Tapu Fini. It works on only one move, Nature's Madness, and only works for them. Z-Moves also have completely arbitrary effects when used to transform non-damaging moves into Z-Moves (each effect is unique to each non-damaging move, though they tend to follow the theme of the move). And in that case, the original effects of the non-damaging move *still happen*.

There are also some bizarrely specific effects for Z-Crystals that you may not have noticed:

* Holding a Z-Crystal prevents Rayquaza from mega-evolving
* Arceus's type changes when holding a Z-Crystal, but Silvally's does not (NEEDS CONFIRMATION)

But we're not here to talk about most of that. Today we're talking about how you work out the Base Power of a Z-Move that's going to do damage.

Firstly, how do you know a Z-Move is going to do damage? In Pokémon, many moves have a Base Power. Higher Base Power means it will do more damage when used by the same Pokémon against the same opposing Pokémon. (I won't get into the myriad other modifiers that take effect afterwards, but you can look into it here if you want to learn more.) Moves that don't have a Base Power - often referred to as status or non-damaging moves - have some other arbitrary effect, but don't actually cause any damage to the opposing Pokémon. Thunder Wave, for example, paralyzes your opponent but does no damage to them.

Any move that has Base Power will become a damaging Z-Move. Which move it becomes (Breakneck Blitz vs Tectonic Rage vs any of the others) is determined by the original move's type. If you're like me, when you played Pokemon Sun & Moon, you generally went by the rule of thumb that Z-Moves do "a lot of damage"™.

But how much exactly? And how will PokémonCompDB tell me how strong a given Z-Move is?

This brings me to my favorite sentence on all of Bulbapedia:

> With the exceptions of Mega Drain (120), Weather Ball (160), Hex (160), Gear Grind (180), V-create (220), Flying Press (170), and Core Enforcer (140), the powers of the type-specific damaging Z-Moves follow the following conversion table for moves that have fixed base powers.

Ha! *Ha!* Now that's a bit of a mindbender.

I'll be honest, PokémonCompDB doesn't support Z-Moves properly yet, partially because of this bonanza of rules that I need to create a system for understanding, representing, and displaying (displaying being the most challenging).

