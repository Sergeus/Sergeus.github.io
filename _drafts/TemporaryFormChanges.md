---
title: Consistency in Temporary Form Changes
inline_title: true
---

I've talked about temporary form changes before when I was talking about Rotom. They're when a Pokémon changes form for a bounded amount of time, often just for the duration of a battle. Today I'm going to be talking about how [PokémonCompDB](/pokemoncompdb.html) represents all of these temporary form changes and some inconsistencies about how to effectively represent them that still plague me to this day.

Mega evolution is the most common temporary form change, available on 46 different Pokémon. It's activated by the player during battle and is only available when the Pokémon is holding the correct mega stone for its species. Also each team can only have one Pokémon mega evolve per battle. (So even if I have Gengar holding Gengarite, if my Blaziken holding Blazikenite has already mega evolved this battle, then Gengar can't.) In PokémonCompDB, a set holding a mega stone is represented by the icon for its mega evolution so it's easy to pick your intended megas out of the lineup:

// image of a team with a mega

This is a fairly effective way of representing a temporary form changes to the user. However, there are other Pokémon that undergo temporary form changes that I don't necessarily want to represent the same way.

Let's take a look at Darmanitan.

// image of darmanitan
*Because who wouldn't want to look at this cuddly ball of fire?*

*Some* Darmanitan can change form mid battle (specifically the ones that have the Zen Mode ability). You find Darmanitan with Zen Mode in Generation 5 (Black & White). All of the other Darmanitan you find will have the ability Sheer Force instead. Zen Mode activates when Darmanitan has less than 50% of its HP remaining, at which time it turns into the Fire/Psychic Zen Darmanitan:

// image
*Clearly*

In a coincidence with how mega evolutions work, Darmanitan that have the Zen Mode ability are represented in PokémonCompDB by their Zen Mode sprite:

// image

This is... reasonable, I'd say. It wouldn't necessarily have been my first instinct were I designing for Darmanitan directly, but it does allow the user to tell apart Zen Mode and Sheer Force Darmanitan at a glance, and they perform quite different roles. (Though the same could be said about many different sets of Latios, of which you can only differentiate the mega ones.)

However, there are some other Pokémon with temporary form changes that it makes less sense to represent by their temporary form. Aegislash and Cherrim are two of the first that come to mind. Aegislash changes back and forth between Shield and Blade forms during battle - into Blade form when it uses an attack that does damage and back into Shield form when it uses King's Shield. Aegislash starts in Shield form and is generally represented in the games by its Shield form sprite. But PokémonCompDB uses the Blade form sprite, because it has a temporary form change (caused by its ability), just like Darmanitan and all those mega evolutions are temporary form changes.

// aegislash sprite image

This makes less sense. *All* Aegislash use the Stance Change ability to change back and forth - the presence of Blade form isn't something the user really cares about. Likewise with Cherrim, it changes into its Sunshine form when the Strong Sunlight weather is in play, through its Flower Gift ability. Like Aegislash, *all* Cherrim do this - so representing it with its Sunshine form isn't particularly expected. But that's what I've ended up doing.

// cherrim image

Then there's Castform. Castform changes form based on the weather - a temporary form change - but it has four different forms: Normal, Sunny, Rainy, and Snowy. With Cherrim and Darmanitan and all the mega evolutions, PokémonCompDB can assess the user's *intent* to use one of the forms by which item or ability they've selected. Castform itself may have Rain Dance, which would suggest Rainy form. Or you might have *another Pokémon* on the same team with Drought (Groudon, Torkoal, Mega Charizard Y, or Ninetales), which would suggest Sunny Form. You might use both and be changing Castform back and forth! Your *opponent* might use a Pokémon with Snow Warning and turn *your* Castform into Snowy form!

// images of castform

Which one do I choose!? The answer is, of course, I don't. Castform remains represented by his normal form, because figuring out all of the above would be crazy.