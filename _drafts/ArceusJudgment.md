---
title: Arceus and Judgment
inline_title: true
---

Arceus, the God Pokémon, is one of the strongest Pokémon around. Its mythology suggests that it created the entire Pokémon universe. It can change into any type. The event item that was supposed to make Arceus available back in Generation 4 (Diamond & Pearl) was never released, making him obtainable only through time-limited event distributions over Mystery Gift and the like in the years since.

// image of Arceus

Today, I'm going to talk about why Arceus's type changing is a bit bananas.

Arceus is a Normal Type Pokémon by default. When Arceus was introduced, 17 new items were also introduced at the same time: the elemental plates. There was one for each type aside from Normal: the Flame Plate for Fire, the Splash Plate for Water, and so on. While holding one of these Plates, Arceus changes into the appropriate type. This is all driven by Arceus's ability: Multitype.

When Arceus changed type, its signature move, Judgment, also changed type to match. Between Judgment's massive base power, Arceus's extremely high attacking stats, the boost to moves of that type provided as a side effect of the Plate, and the Same Type Attack Bonus Arceus gets from being the same type as the move it's using, Judgment tends to hit very hard.

// image

Supporting all of these type changing shenanigans in the Generation 6 (X & Y) version of PokémonCompDB went quite well. In fact, Genesect was added in Generation 6 and did a similar thing. Genesect's changes form when given one of four Drive items: Burn Drive, Douse Drive, Shock Drive, Chill Drive. While holding the respective Drive, the type of Genesect's signature move Techno Blast changed to match the Drive (though Genesect's type remained the same).

// image of genesect

All is well! The item triggers a form change, the form dictates the type of each Pokémon's signature move, and they both work flawlessly!

Then, as further vindication of this system, Silvally was added in Generation 7 (Sun & Moon). It can *also* change its type to match a set of held items, one for each type, and its signature move Multi-Attack changes type! Perfect!

// image
*You know this doesn't work out like it looks like it can*

Silvally, and its pre-evolution Type: Null (great, a Pokémon species with a space, the word "null", *and* a colon in its name!) caused a massive debate among fans when they were first revealed before Sun & Moon's launch. Type: Null's muzzle has a few symbols adorning it that fans claimed were reminiscent of symbols seen representing Arceus in previous games.

When Sun & Moon did release, it's pretty much all confirmed to be true. We find out in-game that Type: Null, mythology wise, is a man-made Pokémon (much like Mewtwo was cloned from Mew), made by scientists trying to recreate the ultimate Pokémon (three guesses who that is). Silvally's ability, mirroring Arceus's Multitype, was even more evidence. And then Silvally's ability was called RKS System.

The pronunciation of Arceus's name has had a bit of a history. Fans, the game Pokémon Battle Revolution, and Dr. Gregory House seemed to have arrived at a consensus of "ar'see'us". Then the Pokémon movie Arceus and the Jewel of Life was released and that localization used the pronunciation "ar'say'us". And after *both* of those, official confirmation of a third, canonical pronunciation was revealed in a Pokémon.com email blast: "ark'ee'us".

I'll let you say "ark'ee'us" and RKS out loud to work that one out. Game Freak loves us, really.

// image

Back to the data structure of all of this. Generation 7 threw another curveball at me. Z-Crystals, the items that allow Pokémon to use Z-Moves, which I've talked about before, *also* interact with Arceus. While holding a Z-Crystal, Arceus's type changes as if he's holding the corresponding Plate. This is our first problem: PokémonCompDB recorded *the* name of the item that caused a form change. Suddenly both Flame Plate *and* Firium Z turn Arceus into its Fire type form.

Brilliant - so my database structure needed to change. You can now have many items that change a Pokémon's form. Fine, then everything works like it did before, right?

The next curveball: when Arceus changes type due to a Z-Crystal, Judgment doesn't change type. Bwuh?

// image

You've got to be *kidding* me! Game Freak are just messing with me at this point. So my form type override system no longer makes sense. It's an *item* type override for specific forms. Back to the drawing board for how *that* system works.

You might be wondering how I realized this was a problem, when my system was chugging happily along before, incorrectly changing Judgment's type when Arceus was holding a Z-Crystal. I was actually looking into *another* edge case, which led me to this one.

// image

There are a series of abilities that change the type of Normal Type moves to a different type (and as of Generation 7 they also boost those moves' power): Aerilate, Galvanize, Pixilate, and Refrigerate. Normal Type moves used by Pokémon with those abilities change to Flying, Electric, Fairy, and Ice respectively. I've been looking into what it would take to support some of the gameplay effects of abilities that are relevant to PokémonCompDB, since at the moment it only actually gives you any feedback on abilities that change your Pokémon's form (like Zen Mode affects Darmanitan, which I've discussed before).

Judgment, Techno Blast, and Multi-Attack are all Normal Type moves by default. Neither Arceus, Silvally, nor Genesect can have any of the above type changing abilities permanently, but *I've learned my lesson*. I need to find out what happens if you somehow give one of those Pokémon that ability and what the game does.

How would you do that? Well, what if you take your Arceus to visit the move tutor in Heart Gold or Soul Silver and teach it Role Play? (Role Play replaces the user's ability with the target's.) Then import it all the way up to at least Generation 6 (I have posts about how to do that, Heart Gold & Soul Silver are in Generation 4) and have your Arceus use Role Play against an opposing Mega Salamence that has Aerilate?

Nothing happens. Judgment is unaffected.

// image

Great! Just *great*! So there's a priority system behind all of these type changes as well!

Fine! PokémonCompDB will support that too! Because I'm certifiably insane!