---
title: The Many Forms of Pikachu
inline_title: true
---

Pikachu, the electric rodent Pokémon and one of the best known mascots of any series in the world, has been represented in the main series Pokémon games since the very beginning. There have also been many different iterations of the adorable little guy, to celebrate a variety of Pokémon-related occasions. Last week I talked about forms and Rotom, and today, I'm going to talk about the variant forms of Pikachu that have had the most impact on [PokémonCompDB](/pokemoncompdb.html) and how they create their own unique spins on the normal Pokémon.

Pikachu was also recently [appointed as an ambassador of the real life city of Osaka, Japan](https://www.theverge.com/2017/11/30/16720968/pikachu-ambassador-of-osaka-japan-hello-kitty):

![](/assets/img/pikachu-osaka.jpg){:style="max-height:250px;"}
*Image courtesy of [Foreign Minister of Japan] Taro Kono's Twitter feed*

The first thing we want to look at is normal Pikachu. What does that actually look like?

![](/assets/img/pikachu.PNG){:style="max-height:200px;"}
*Adorable and infinitely recognizable*

Pikachu, like other Pokémon I've discussed before, was given a pre-evolution in Pichu in Generation 2 (Gold & Silver). Also as I've discussed before, Pikachu evolves via an evolutionary stone (the Thunder Stone) into Raichu. So like Arcanine, described in my previous post, Pikachu learns most of the level up moves and Raichu does not (to discourage players from evolving Pikachu immediately). Raichu also has an Alolan variant form, when it evolves from Pikachu in the Generation 7 games (Sun, Moon, Ultra Sun, & Ultra Moon). This caused its own set of problems for me in how Alolan form evolutions are handled, as described here.

// table of three non-pikachu guys

But that's enough plugging my own past blog posts. What's unique about Pikachu? Even before we consider the special forms, there are some wrinkles about normal Pikachu. Pikachu can learn the move Volt Tackle, but only by breeding a Pikachu that's holding a Light Ball. (Which is something I realized while writing this post that PokémonCompDB does not support, it doesn't realize the Light Ball is needed at all. That will need fixing.)

Pikachu is also one of the Pokémon that has visible gender differences. Ever since Generation 4 (Diamond & Pearl), male Pikachu have a straight-edged tail and female Pikachu have a little heart shape on the end. It's not the most subtle Pokémon gender dimorphism out there, but it's certainly easy to miss:

// image of genders side by side

But what about the form differences? One of the iconic ones (at least in my mind) is Surfing Pikachu, who was accessible through a variety of events in the late 90s to early 2000s, as well as through some of the side series games on the Nintendo 64 (Pokémon Stadium & Pokémon Stadium 2) and the GameCube (Pokémon Colosseum & Pokémon XD: Gale of Darkness). It also makes a reappearance in Pokémon Ultra Sun & Ultra Moon as a prize you can earn from the Mantine Surfing mini-game.

From a PokémonCompDB perspective, Surfing Pikachu isn't very complicated. It's a "Special Move" much like many other event-distribution-only moves learned by other Pokémon (and there are a lot of those). If the user wants to have a Pikachu with Surf, then we'll just let them under the assumption they'll know how to get one (some possible sources will be listed).

// surfing pikachu image

The first variant that turned out to be a pain was Cosplay Pikachu. Cosplay Pikachu is a specific Pikachu given to the player in Pokémon Omega Ruby & Alpha Sapphire. It's able to be dressed up in different costumes (hence the name) and in each of those costumes it learns a signature move for that costume. (Pikachu Libre, the luchador costume, is also the only time any Pokémon aside from Hawlucha learns Flying Press.) In this way, it's exactly like Rotom from last week, even though the player can swap back and forth between its forms (costumes) at will, those specific moves are restricted to individual forms.

Notably, Cosplay Pikachu still looks different from normal Pikachu even when it isn't wearing a costume. The end of its tail is black, instead of the usual yellow all the way. The Cosplay Pikachu the player receives is also always female, so PokémonCompDB needs to reflect that restriction, which is sort of a reversed version of what happens with Meowstic's forms being quite different between male and female (unlike most Pokémon gender differences, which are purely cosmetic).

Cosplay Pikachu also doesn't evolve. This has proved to be particularly annoying, because Pichu learns some moves that Pikachu doesn't (in Sun & Moon that's Charm, Sweet Kiss, and Nasty Plot), which are pre-evolution only moves for Pikachu normally, but instead need to be marked as unavailable for Cosplay Pikachu. Also reflecting the fact that it can't evolve, Eviolite, the item that makes not-fully-evolved Pokémon stronger, works for normal Pikachu but not Cosplay Pikachu.

// image

I actually *missed* Cosplay Pikachu completely when creating the PokémonCompDB database for Generation 6 (X & Y) originally. I backtracked to it when I realize that the different Cap Pikachu forms in Generation 7 (Sun & Moon) weren't being supported correctly.

The Cap Pikachu forms are Pikachu that were distributed through an event online celebrating Pokémon's 20th anniversary and the release of the movie [Pokémon the Movie: I Choose you!](https://en.wikipedia.org/wiki/Pok%C3%A9mon_the_Movie:_I_Choose_You!). (Many of the event distributions tie into Pokémon movie debuts that feature the Pokémon being distributed.) The event was a bit strange, in that 6 of the 7 Cap Pikachu forms were distributed across 6 weeks. There was a single code that redeemed them and which Cap you received depended on which week you redeemed that code in. A single game could only receive *one* of the six available Cap Pikachu through the event. (If you had many copies of the games, you could trade all 6 into the same game after receiving them all separately.)

Why Pikachu in a cap? This is a callback to the Pokémon anime, which has been running alongside the games since 1997 and centers around Ash Ketchum, a Pokémon trainer who travels with a Pikachu. Each cap is a cap that Ash wore in a specific season (or seasons) of the show, which corresponded to a region of the Pokémon world. Starting with Kanto from Generation 1 (Red & Blue) and ending in Alola in Generation 7 (Sun & Moon). The Partner Cap Pikachu (the 7th of the 7 cap variants) is available only in Ultra Sun & Ultra Moon, by scanning the QR code on the back of a collectible Pikachu trading card given to people who attended cinema screenings of the I Choose You! movie.

// caps image
*Obtaining all of these became extremely elaborate and required traveling potentially significant distances in physical reality*

Cap Pikachu was based on Ash's Pikachu from the show and its move set included several moves that Pikachu otherwise couldn't learn. And which move it is varies based on which cap you've got! The Hoenn, Sinnoh, Unova, Kalos, and Unova Cap Pikachu all know Iron Tail, which Pikachu cannot otherwise learn. The Z-Move 10,000,000 Volt Thunderbolt is also only available to Cap Pikachu holding the Pikashunium Z Z-Crystal (which I talked about briefly before). This Z-Crystal transforms the move Thunderbolt, which normal Pikachu *can learn*, into its Z-Move variant, so PokémonCompDB needs to track Z Crystals that work only on specific forms for this (and Aloraichium Z, which only works for Alolan Raichu, not normal Raichu.)

Like Cosplay Pikachu, Cap Pikachu cannot evolve (much like Ash's Pikachu hasn't evolved in the anime, which was the subject of an episode early on). It's not affected by Eviolite. And of course, since Ash's Pikachu in the anime is male, all of the Cap Pikachu received through the event distribution are also male.

Seemingly in an effort to test the correctness of my database, Game Freak has made normal Pikachu's *other* species-specific Z-Move, Catastropika from the Z-Crystal Pikanium Z, a transformed version of the move Volt Tackle. I'm sure you remember that I mentioned Volt Tackle above, as a move that Pikachu learns by hatching from an egg when one of its parents was holding a Light Ball. Since you can never hatch a Cap Pikachu (you can only receive it from the event), it's impossible to obtain a Cap Pikachu that knows Volt Tackle. That makes the Catastropika Z-Move implicitly exclusive to non-Cap-Pikachu.

In a nice little additional wrinkle, the move Iron Tail, known by the specific Cap Pikachu forms I mentioned above, is the only damaging Steel type move known by a form of Pikachu in Sun & Moon. So only those Pikachu can use the damaging Steel type Z-Move, Corkscrew Crash.

// image

There are many more forms of Pikachu. These are just the ones that have caused me trouble thus far. Many of them, like other unique forms that interact with specific features that are exclusive to certain versions of the core Pokémon series games, are locked into the game they can be received in. Unlike other normal Pokémon they can't be imported to the next set of games (brought over from one generation to the next). And for this, I am eternally grateful.