---
title: Consistency in Temporary Form Changes
inline_title: true
---

I've talked about temporary form changes before [when I was talking about Rotom](({% post_url 2017-12-9-RotomForms %})). They're when a Pokémon changes form for a bounded amount of time, often just for the duration of a battle. Today I'm going to be talking about how [PokémonCompDB](/pokemoncompdb.html) represents all of these temporary form changes and some inconsistencies about how to effectively represent them that still plague me to this day.

Mega evolution is the most common temporary form change, available on [46 different Pokémon](https://bulbapedia.bulbagarden.net/wiki/Mega_Evolution). It's activated by the player during battle and is only available when the Pokémon is holding the correct [mega stone](https://bulbapedia.bulbagarden.net/wiki/Mega_Stone) for its species. Also each team can only have one Pokémon mega evolve per battle. (So even if I have [Gengar](https://www.serebii.net/pokedex-sm/094.shtml) holding [Gengarite](https://www.serebii.net/itemdex/gengarite.shtml), if my [Blaziken](https://www.serebii.net/pokedex-sm/257.shtml) holding [Blazikenite](https://www.serebii.net/itemdex/blazikenite.shtml) has already mega evolved this battle, then Gengar can't.) In PokémonCompDB, a set holding a mega stone is represented by the icon for its mega evolution so it's easy to pick your intended megas out of the lineup:

![](/assets/img/pokemoncompdb-team-with-mega.PNG)
*Mega Blastoise on the small team preview of a single team in PokémonCompDB*

This is a fairly effective way of representing a temporary form changes to the user. However, there are other Pokémon that undergo temporary form changes that I don't necessarily want to represent the same way.

Let's take a look at [Darmanitan](https://www.serebii.net/pokedex-sm/555.shtml).

![](/assets/img/darmanitan.png){:style="max-height:200px;"}
*Because who wouldn't want to look at this cuddly ball of fire?*

*Some* Darmanitan can change form mid battle (specifically the ones that have the [Zen Mode](https://www.serebii.net/abilitydex/zenmode.shtml) ability). You find Darmanitan with Zen Mode in Generation 5 (Black & White). All of the other Darmanitan you find will usually have the ability [Sheer Force](https://www.serebii.net/abilitydex/sheerforce.shtml) instead. Zen Mode activates when Darmanitan has less than 50% of its HP remaining, at which time it turns into the Fire/Psychic Zen Darmanitan:

![](/assets/img/darmanitan-zen.png){:style="max-height:200px;"}
*Clearly*

In a coincidence with how mega evolutions work, Darmanitan that have the Zen Mode ability are represented in PokémonCompDB by their Zen Mode sprite:

![](/assets/img/pokemoncompdb-darmanitan-team.PNG)
*One of each, forming the greatest team anyone has ever seen*

This is... reasonable, I'd say. It wouldn't necessarily have been my first instinct were I designing for Darmanitan directly, but it does allow the user to tell apart Zen Mode and Sheer Force Darmanitan at a glance, and they perform quite different roles. (Though the same could be said about many different sets of [Latios](https://www.serebii.net/pokedex-sm/381.shtml), of which you can only differentiate the mega ones.)

As a quick interlude, you might be thinking that these tiny little sprite images seem like they wouldn't take up much space and why is a whole team represented like that when there's so much screen space to use. The answer is that these are small team previews shown when listing all of your teams. If you click on any and get the full team page, you'll see something more like this:

![](/assets/img/pokemoncompdb-team-summary.PNG){:style="max-height:300px;"}
*And clicking through a single one gives you **even more** information*

However, there are some other Pokémon with temporary form changes that it makes less sense to represent by their temporary form. [Aegislash](https://www.serebii.net/pokedex-sm/681.shtml) and [Cherrim](https://www.serebii.net/pokedex-sm/421.shtml) are two of the first that come to mind. Aegislash changes back and forth between Shield and Blade forms during battle - into Blade form when it uses an attack that does damage and back into Shield form when it uses [King's Shield](https://www.serebii.net/attackdex-sm/king'sshield.shtml). Aegislash starts in Shield form and is generally represented in the games by its Shield form sprite. But PokémonCompDB uses the Blade form sprite, because it has a temporary form change (caused by its ability), just like Darmanitan and all those mega evolutions are temporary form changes.

![](/assets/img/pokemoncompdb-aegislash-team.PNG)
*This annoys me more than I can say*

This makes less sense. *All* Aegislash use the [Stance Change](https://www.serebii.net/abilitydex/stancechange.shtml) ability to change back and forth - the presence of Blade form isn't something the user really cares about. Likewise with Cherrim, it changes into its Sunshine form when the Strong Sunlight weather is in play, through its [Flower Gift](https://www.serebii.net/abilitydex/flowergift.shtml) ability. Like Aegislash, *all* Cherrim do this - so representing it with its Sunshine form isn't particularly expected. But that's what I've ended up doing.

![](/assets/img/cherrim-forms.png){:style="max-height:200px;"}
*Overcast and Sunshine Cherrim, because even changes to the weather affect Pokémon*

Then there's [Castform](https://www.serebii.net/pokedex-sm/351.shtml). Castform changes form based on the weather - a temporary form change - but it has four different forms: Normal, Sunny, Rainy, and Snowy. With Cherrim and Darmanitan and all the mega evolutions, PokémonCompDB can assess the user's *intent* to use one of the forms by which item or ability they've selected. Castform itself may have [Rain Dance](https://www.serebii.net/attackdex-dp/raindance.shtml), which would suggest Rainy form. Or you might have *another Pokémon* on the same team with [Drought](https://www.serebii.net/abilitydex/drought.shtml) ([Groudon](https://www.serebii.net/pokedex-sm/383.shtml), [Torkoal](https://www.serebii.net/pokedex-sm/324.shtml), [Mega Charizard Y](https://www.serebii.net/pokedex-sm/006.shtml#megaevo), or [Ninetales](https://www.serebii.net/pokedex-sm/038.shtml)), which would suggest Sunny Form. You might use both and be changing Castform back and forth! Your *opponent* might use a Pokémon with [Snow Warning](https://www.serebii.net/abilitydex/snowwarning.shtml) and turn *your* Castform into Snowy form!

| Normal | Sunny | Rainy | Snowy |
:-------:|:-----:|:-----:|:------:
| ![](/assets/img/castform-normal.png){:style="max-height:200px;"} | ![](/assets/img/castform-sunny.png){:style="max-height:200px;"} | ![](/assets/img/castform-rainy.png){:style="max-height:200px;"} | ![](/assets/img/castform-snowy.png){:style="max-height:200px;"} |

Which one do I choose!? The answer is, of course, I don't. Castform remains represented by his normal form, because figuring out all of the above would be crazy.