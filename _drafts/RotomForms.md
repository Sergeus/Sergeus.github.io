---
title: Rotom Forms
inline_title: true
---

[Rotom](https://www.serebii.net/pokedex-sm/479.shtml) is a tiny little Electric/Ghost Pokémon that is pretty adorable. It also acts as an infuriating sidekick in Generation 7 (Sun, Moon, Ultra Sun, & Ultra Moon). Rotom changes form between several different types and drastically different stats by possessing household appliances. (Yes, this is actually what it does.) There are a lot of Pokémon that change form (some of which I've talked about before), but Rotom was the first Pokémon I encountered that had certain moves only available in certain forms, but could also switch between forms at will.

A little more background will probably help so that makes more sense. This is Rotom:

![](/assets/img/rotom.png){:style="max-height:200px;"}
*It is totes adorbs and wants to possess your lawnmower*

Pokémon "change form" for a lot of different reasons. Usually form changes take one of three major categories (though, like everything else, there are exceptions): temporary, repeatable, and locked in. (Not official names.) Any form change always comes with a visual difference to distinguish the Pokémon from its other forms.

Notably, I'm not using the word "transformations" to avoid confusion with Transform and Ditto. That's a different thing. (Because of course it is.)

Temporary form changes are where a Pokémon can change its attributes for a specific window of time. These attribute changes mostly include stats and typing changes. Most of them last for the duration of a battle. Mega-evolution is a common temporary form change, such as with Absol becoming Mega-Absol.

//Absol and mega pic
*Two points if you guess which one is which*

Other mid-battle temporary form changes include Darmanitan (when it has the Zen Mode ability) and Aegislash. There are also some temporary form changes that last beyond a single battle, such as Furfrou (whose cosmetic-only form change of its fur being trimmed lasts 5 days of real world time) and Shaymin (whose change into Sky Form only works between 5am and 8pm and lasts until 8pm, or when it gets Frozen).

// furfrou
*There are just... so many hairstyles*

Repeatable form changes are ones where the Pokémon can be intentionally changed between its different available forms at a time of the player's choosing. I've mentioned this in a [previous post]() // NEEDS LINKING about Deoxys. This also includes some other Pokémon like Tornadus.

// tornadus pic

From [PokémonCompDB](/pokemoncompdb.html)'s perspective, repeatable form changes mean that the player can let a single Pokémon access all of every form's moves. Deoxys learns different moves by level up in each form, but the player can always switch to the form they want to learn the move from and learn that one. So I don't need to put many restrictions on the user's choice of move based on form. It still works even if the player wants two moves that Deoxys learns at the same level in different forms. (For example, it learns Knock Off at level 19 in Sun & Moon in Normal Form and Taunt at level 19 in Attack Form, and the player may want both Knock Off and Taunt.) To achieve that, they learn one by level up, then switch forms to the other and use the Move Reminder to learn the other move. That complexity actually makes my life easier, just treat these Pokémon's learn sets as all one big pool.

The last main kind of form change are the locked in ones. For some Pokémon, when you have one of a specific form, it will always stay in that form. Lycanroc and Vivillon are examples of this. A Dusk Form Lycanroc can never be changed into one of the other two. A Meadow Pattern Vivillon can never change to one of the other patterns.

// Vivillon pic
*There are a lot of patterns of Vivillon. The forms are cosmetic-only, so of course I care about representing them correctly.*

Some locked in forms learn different moves from their counterparts. And since in PokémonCompDB the user is allowed to *change their mind* and switch which form of Pokémon they're intending to use, it needs to make sure that if you choose to change the form of a set and it has some moves that the other form can't learn, those moves should be removed first.

So those are the main type of form changes. Rotom is of the repeatable variety. Like I said at the beginning, Rotom possesses appliances to change form, which the player can do by finding those appliances in the world. It looks like this:

// forms of rotom table

However, I mentioned above that Deoxys, who is also a repeatable form change Pokémon, has some complexity that makes my life easier. Because you can switch back and forth between the different forms of Deoxys whenever you want, a single Deoxys can learn all of the moves from any of its forms. Rotom is *mostly* like that. Except each of its forms has a signature move. 

(LIST OF SIGNATURE MOVES HERE) And when Rotom changes form, it *forgets* the signature move of its previous form. So you can't have a Frost Rotom with Hydro Pump (Wash Rotom's signature move). This meant that unlike all of the other repeatabvle form change Pokémon, Rotom needed an exception for its form signature moves, that made Rotom behave like a locked in form change, for just those moves.

I got this working back in Generation 6 (X & Y), where I thought Rotom was the only instance of this behavior. But coming into Generation 7 (Sun & Moon), I realized that Game Freak had some more subtle usages of this kind of repeatable-form-change-specific move behavior, which will be the subject of another post soon!

// pikachu pic
*There are more Pikachu than you might expect*