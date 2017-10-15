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

Ha! *Ha!* Now that's a bit of a mindbender. It perfectly captures the insanity of trying to fit Pokémon into a neat little box of data.

I'll be honest, PokémonCompDB doesn't support Z-Moves properly yet, partially because of this bonanza of rules that I need to create a system for understanding, representing, and displaying (displaying being the most challenging).

So, let's deconstruct that sentence to work out what it actually means.

> With the **exceptions of Mega Drain (120), Weather Ball (160), Hex (160), Gear Grind (180), V-create (220), Flying Press (170), and Core Enforcer (140)**, the powers of the type-specific damaging Z-Moves follow the following conversion table for moves that have fixed base powers.

Straight off the bat, these 7 moves follow no pattern at all and if you turn them into a Z-Move then you'll get an arbitrary base power (listed next to them in the quote). It's fixed for each move and I'll need to straight up associate a specific Z-Move Base Power with each of these individually.

Why these 7? V-create and [Core Enforcer](https://www.serebii.net/attackdex-sm/coreenforcer.shtml) are signature moves of two legendary Pokémon, Victini and [Zygarde](https://www.serebii.net/pokedex-sm/718.shtml) respectively. (Though there was a Rayquaza distributed through an event in Japan during Generation 5 that knew V-create, so I'll inevitably end up listing that too!) [Gear Grind](https://www.serebii.net/attackdex-bw/geargrind.shtml) is the signature move of the [Klingklang](https://www.serebii.net/pokedex-sm/601.shtml) evolutionary line. [Mega Drain](https://www.serebii.net/attackdex-sm/megadrain.shtml) and [Hex](https://www.serebii.net/attackdex-sm/hex.shtml) are very widely distributed. [Weather Ball](https://www.serebii.net/attackdex-xy/weatherball.shtml) was once exclusive to [Castform](https://www.serebii.net/pokedex-sm/351.shtml) (in Generation 3) but has since become available on many others. And finally [Flying Press](https://www.serebii.net/attackdex-sm/flyingpress.shtml) is a signature move of [Hawlucha](https://www.serebii.net/pokedex-sm/701.shtml) (though the special event [Pikachu Libre](https://www.serebii.net/pokedex-xy/025.shtml) in Generation 6 also knows it).

There doesn't *really* seem to be a consistent pattern here. Some are unique to certain Pokémon and others aren't. Some are physical and some are special. They're from a random selection of types. They're not all very powerful or all very weak. They were introduced at different times throughout the series (Weather Ball is from Generation 3 and Core Enforcer is new in Generation 7, with the others scattered in between). There's no real "theme" uniting them all.

I don't really know why these 7 moves are different. But they are! So we'll move on to the next part of the sentence:

> With the exceptions of Mega Drain (120), Weather Ball (160), Hex (160), Gear Grind (180), V-create (220), Flying Press (170), and Core Enforcer (140), **the powers of the type-specific damaging Z-Moves** follow the following conversion table for moves that have fixed base powers.

So this information is only valid for the Z-Moves that are type-specific and damaging. Non-damaging Z-Moves (such as Z-Thunder Wave) do their own thing. Damaging Z-Moves that aren't type-specific (like Stoked Sparksurfer on Alolan Raichu, from the Aloraichium Z Z-Crystal) also do their own thing.

This part makes sense - the non-damaging Z-Moves are conceptually separate. The non-type-specific Z-Moves are used to call out famous and special Pokémon and make them feel more empowered. It makes sense that those moves can also diverge from the patterns of other Z-Moves. (Though I'll need to store that information as well!)

Next up:

> With the exceptions of Mega Drain (120), Weather Ball (160), Hex (160), Gear Grind (180), V-create (220), Flying Press (170), and Core Enforcer (140), the powers of the type-specific damaging Z-Moves **follow the following conversion table** for moves that have fixed base powers.

Here's the table they're talking about:

| Normal Base Power | Z-Move Base Power |
|:-----------------:|:-----------------:|
| 0-55              | 100               |
| 60-65             | 120               |
| 70-75             | 140               |
| 80-85             | 160               |
| 90-95             | 175               |
| 100               | 180               |
| 110               | 185               |
| 120-125           | 190               |
| 130               | 195               |
| 140+              | 200               |

If, like me, you were caught off guard by this table not being contiguous, know that the Base Power of all fixed Base Power moves in Pokémon is divisible by 5. (Can't wait until *that* changes at some point!)

So the Base Power of the Z-Move varies depending on which move was turned into it. From an experience point of view, this makes a lot of sense. I expect Hyper Beam turned into a Z-Move to do more damage than Tackle, even if they both become a Z-Move with the same name (Breakneck Blitz).

It's interesting that the progression isn't linear. Or even particularly consistent. But it does follow the "higher does more damage" pattern you would expect as a player.

// graph here

Interestingly if you have a high enough Base Power move to start with (more than 200), turning a move into a Z-Move causes it to do less damage. The only move with high enough Base Power for this to happen is Explosion becoming Breakneck Blitz.

As you might expect, Struggle can't become a Z-Move, because there's no real way in the game to tell your Pokémon to do that.

And at last, the final piece:

> With the exceptions of Mega Drain (120), Weather Ball (160), Hex (160), Gear Grind (180), V-create (220), Flying Press (170), and Core Enforcer (140), the powers of the type-specific damaging Z-Moves follow the following conversion table **for moves that have fixed base powers**.

Everything we've just talked about for the conversion table and the special exceptions and damaging moves only applies to moves with fixed Base Power. Some moves have their Base Power vary mid-battle. Gyro Ball does more damage the slower the user is than its target, for example. Flail does more damage the less HP the user has. Present's damage is random. And many others! Z-Moves from these variable Base Power moves are... not described in Bulbapedia.

// research about what variable base power moves do

And there we have it! You (and I) now understand how to calculate the Base Power of a Z-Move you'll get from using a Z-Crystal on a given damaging move. Because that was *way* more complicated than I thought it would be going in!