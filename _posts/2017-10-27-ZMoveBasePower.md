---
title: Z-Move Base Power
inline_title: true
image_meta: /assets/img/z-move-meta.jpg
---

[Z-moves](https://bulbapedia.bulbagarden.net/wiki/Z-Move) are one of the new headline features in Generation 7 (Sun & Moon). There are quite a few unique things about them compared to... pretty much every other move that's come before. They can be used, only once per battle, to transform one of your Pokémon's existing moves into a more powerful Z-Move, using the Z-Move instead of the original move. They're unlocked by a special item called a [Z-Crystal](https://www.serebii.net/itemdex/list/zcrystal.shtml) that the Pokémon must be holding, with one Z-Crystal available per type. <sup>(And a few that are only for specific Pokémon like [Pikashunium Z](https://www.serebii.net/itemdex/pikashuniumz.shtml) for Pikachu.)</sup> They have hugely different effects based on which normal move you turn into a Z-Move.

![](/assets/img/pikachu-z-move-dance.gif)
*Fancy dance moves are also involved*

Along with a couple of Pokémon-specific Z-Crystals, there is a grand total of one Z-Crystal that can be used by *multiple **specific*** Pokémon: [Tapunium Z](https://www.serebii.net/itemdex/tapuniumz.shtml), which is used by [Tapu Koko](https://www.serebii.net/pokedex-sm/785.shtml), [Tapu Lele](https://www.serebii.net/pokedex-sm/786.shtml), [Tapu Bulu](https://www.serebii.net/pokedex-sm/787.shtml), and [Tapu Fini](https://www.serebii.net/pokedex-sm/788.shtml). It works on only one move, [Nature's Madness](https://www.serebii.net/attackdex-sm/nature'smadness.shtml), and only works for them. Z-Moves also have completely arbitrary effects when used to transform non-damaging moves into Z-Moves (each effect is unique to each non-damaging move, though they tend to follow the theme of the move). And in that case, the original effects of the non-damaging move *still happen*.

There are also some bizarrely specific effects for Z-Crystals that you may not have noticed:

* [Arceus](https://www.serebii.net/pokedex-sm/493.shtml)'s type changes when holding a Z-Crystal, but [Silvally](https://www.serebii.net/pokedex-sm/773.shtml)'s does not
* Holding a Z-Crystal prevents [Rayquaza](https://www.serebii.net/pokedex-sm/384.shtml) from mega-evolving

![](/assets/img/sad-rayquaza.png)
*This makes Rayquaza sad*

But we're not here to talk about most of that. Today we're talking about how you work out the Base Power of a Z-Move that's going to do damage.

Firstly, how do you know a Z-Move is going to do damage? In Pokémon, many moves have a [Base Power](https://bulbapedia.bulbagarden.net/wiki/Power). Higher Base Power means it will do more damage when used by the same Pokémon against the same opposing Pokémon. (I won't get into the myriad other modifiers that take effect afterwards, but you can look into it [here](https://bulbapedia.bulbagarden.net/wiki/Damage) if you want to learn more.) Moves that don't have a Base Power - often referred to as "status" or "non-damaging" moves - have some other arbitrary effect, but don't actually cause any damage to the opposing Pokémon. [Thunder Wave](https://www.serebii.net/attackdex-sm/thunderwave.shtml), for example, paralyzes your opponent but does no damage to them.

Any move that has non-zero Base Power will become a damaging Z-Move. Which move it becomes ([Breakneck Blitz](https://www.serebii.net/attackdex-sm/breakneckblitz.shtml) vs [Tectonic Rage](https://www.serebii.net/attackdex-sm/tectonicrage.shtml) vs any of the others) is determined by the original move's type. If you're like me, when you played Pokemon Sun & Moon, you generally went by the rule of thumb that Z-Moves do "a lot of damage"™.

![](/assets/img/continental-crush.png)
*With names like Continental Crush. Yes, it drops a mountain on your opponent.*

But how much damage exactly? And how will [PokémonCompDB](/pokemoncompdb.html) tell me how strong a given Z-Move is?

This brings me to my favorite sentence on all of Bulbapedia:

> With the exceptions of Mega Drain (120), Weather Ball (160), Hex (160), Gear Grind (180), V-create (220), Flying Press (170), and Core Enforcer (140), the powers of the type-specific damaging Z-Moves follow the following conversion table for moves that have fixed base powers.

Ha! *Ha!* Now that's a mindbender. It captures the insanity of trying to fit Pokémon into a neat little box of data.

I'll be honest, PokémonCompDB doesn't support Z-Moves properly yet, partially because of this bonanza of rules that I need to create a system for understanding, representing, and displaying.

So, let's deconstruct that sentence to work out what it actually means.

> With the **exceptions of Mega Drain (120), Weather Ball (160), Hex (160), Gear Grind (180), V-create (220), Flying Press (170), and Core Enforcer (140)**, the powers of the type-specific damaging Z-Moves follow the following conversion table for moves that have fixed base powers.

Straight off the bat, these 7 moves follow no pattern at all and if you turn them into a Z-Move then you'll get an arbitrary base power (listed next to them in the quote). It's fixed for each move and I'll need to straight up associate a specific Z-Move Base Power with each of these individually.

Why these 7? [V-create](https://www.serebii.net/attackdex-sm/v-create.shtml) and [Core Enforcer](https://www.serebii.net/attackdex-sm/coreenforcer.shtml) are signature moves of two legendary Pokémon, [Victini](https://www.serebii.net/pokedex-sm/494.shtml) and [Zygarde](https://www.serebii.net/pokedex-sm/718.shtml) respectively. (Though there was a Rayquaza distributed through an event in Japan during Generation 5 that knew V-create, so I'll inevitably end up listing that too!) [Gear Grind](https://www.serebii.net/attackdex-bw/geargrind.shtml) is the signature move of the [Klingklang](https://www.serebii.net/pokedex-sm/601.shtml) evolutionary line. [Mega Drain](https://www.serebii.net/attackdex-sm/megadrain.shtml) and [Hex](https://www.serebii.net/attackdex-sm/hex.shtml) are very widely distributed. [Weather Ball](https://www.serebii.net/attackdex-xy/weatherball.shtml) was once exclusive to [Castform](https://www.serebii.net/pokedex-sm/351.shtml) (in Generation 3) but has since become available on many others. And finally [Flying Press](https://www.serebii.net/attackdex-sm/flyingpress.shtml) is a signature move of [Hawlucha](https://www.serebii.net/pokedex-sm/701.shtml) (though the special event [Pikachu Libre](https://www.serebii.net/pokedex-xy/025.shtml) in Generation 6 also knows it).

There doesn't *really* seem to be a consistent pattern here. Some are unique to certain Pokémon and others aren't. Some are physical and some are special. They're from a random selection of types. They're not all very powerful or all very weak. They were introduced at different times throughout the series (Weather Ball is from Generation 3 and Core Enforcer is new in Generation 7, with the others scattered in between). There's no real "theme" uniting them all.

I don't really know why these 7 moves are different. But they are! As you'll see throughout this post (and throughout this blog) Game Freak apparently aren't afraid to hand author many, *many* individual data points in their games. So we'll move on to the next part of the sentence:

> With the exceptions of Mega Drain (120), Weather Ball (160), Hex (160), Gear Grind (180), V-create (220), Flying Press (170), and Core Enforcer (140), **the powers of the type-specific damaging Z-Moves** follow the following conversion table for moves that have fixed base powers.

So this information is only valid for the Z-Moves that are type-specific and damaging. Non-damaging Z-Moves (such as Z-Thunder Wave) do their own thing. Damaging Z-Moves that aren't type-specific (like [Stoked Sparksurfer](https://www.serebii.net/attackdex-sm/stokedsparksurfer.shtml) on [Alolan Raichu](https://www.serebii.net/pokedex-sm/026.shtml), from the [Aloraichium Z](https://www.serebii.net/itemdex/aloraichiumz.shtml) Z-Crystal) also do their own thing.

![](/assets/img/snorlax-pulverizing-pancake.png)
*Snorlax has its own unique Z-Move. Yes, it does what it sounds like it does.*

This part is fairly self explanatory - the non-damaging Z-Moves are conceptually separate. The non-type-specific Z-Moves are used to call out famous and special Pokémon and make them feel more empowered. It makes sense that those moves can also diverge from the patterns of other Z-Moves. (Though PokémonCompDB will need to store that information as well!)

Next up:

> With the exceptions of Mega Drain (120), Weather Ball (160), Hex (160), Gear Grind (180), V-create (220), Flying Press (170), and Core Enforcer (140), the powers of the type-specific damaging Z-Moves **follow the following conversion table** for moves that have fixed base powers.

Here's the table they're talking about:

![](/assets/img/z-move-power-table.PNG)

If, like me, you were caught off guard by this table not being contiguous, know that the Base Power of all fixed Base Power moves in Pokémon is divisible by 5. (Can't wait until *that* changes at some point!) And why are 105, 115, 125, and 135 missing? Because there are no moves that have a Base Power of any of those Base Power values in Sun & Moon. (Another thing I'm sure will change eventually and make this table subtly wrong in future games.)

So the Base Power of the Z-Move varies depending on which move was turned into it. As a player thinking about this it makes a lot of sense. I expect Hyper Beam turned into a Z-Move to do more damage than Tackle, even if they both become a Z-Move with the same name (Breakneck Blitz).

It's interesting that the progression isn't completely linear. There is a baseline Base Power of 100 and then has a diminishing increase in Base Power as you go above Base Power 60 with the move being transformed. It generally follows the "higher does more damage" pattern you would expect as a player.

![](/assets/img/z-move-base-power-graph.PNG)
*Fear my Excel graphs!*

Interestingly if you have a high enough Base Power move to start with (more than 200), turning a move into a Z-Move causes it to do less damage. The only move with high enough Base Power for this to happen is [Explosion](https://www.serebii.net/attackdex-sm/explosion.shtml) becoming Breakneck Blitz.

As you might expect, [Struggle](https://www.serebii.net/attackdex-sm/struggle.shtml) (the move a Pokémon uses if it has run out of its other moves) can't become a Z-Move, because there's no real way in the game to tell your Pokémon to do that.

And at last, the final piece:

> With the exceptions of Mega Drain (120), Weather Ball (160), Hex (160), Gear Grind (180), V-create (220), Flying Press (170), and Core Enforcer (140), the powers of the type-specific damaging Z-Moves follow the following conversion table **for moves that have fixed base powers**.

Everything we've just talked about for the conversion table and the special exceptions and damaging moves only applies to moves with fixed Base Power. Some moves have their Base Power vary mid-battle. [Gyro Ball](https://www.serebii.net/attackdex-sm/gyroball.shtml) does more damage the slower the user is than its target, for example. [Flail](https://www.serebii.net/attackdex-sm/flail.shtml) does more damage the less HP the user has. [Present](https://www.serebii.net/attackdex-sm/present.shtml)'s damage is random. And many others!

Z-Moves coming from these variable Base Power moves seem to be arbitrary. Present becomes a Base Power 100 Breakneck Blitz. (Which is lower than Present's own max power of 120.) Gyro Ball becomes a Base Power 160 [Corkscrew Crash](https://www.serebii.net/attackdex-sm/corkscrewcrash.shtml) (regardless of the attacker or defender's Speed). [Magnitude](https://www.serebii.net/attackdex-sm/magnitude.shtml) becomes a Base Power 140 Tectonic Rage (lower than Magnitude's maximum Base Power of 150).

The [list goes on](https://bulbapedia.bulbagarden.net/wiki/Category:Moves_that_have_variable_power), with even more moves that have variable Base Power and seemingly unrelated Base Power in the Z-Move they transform into. So much like the non-type-specific Z-Moves, they appear to be individually authored.

![](/assets/img/snorlax-pulverizing-pancake.png)
*I thought you might like to see this again*

And there we have it! You (and I) now understand how to calculate the Base Power of a Z-Move you'll get from using a Z-Crystal on a given damaging move. There's a lot of detail and seemingly hand-authored individual stats involved in doing "a lot of damage"™.