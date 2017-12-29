---
title: Mega-Evolution Exceptions
inline_title: true
---

Mega evolutions were added to Pokémon in Generation 6 (X & Y). They're effectively temporary form changes that activate in the middle of a battle. When a Pokémon is holding the correct mega stone (for example, Abomasnow holding an Abomasite), the player can elect to transform them into their mega form on their turn. The transformation happens at the beginning of that turn, before any Pokémon in the battle have moved. Mega-evolutions usually drastically increase the stats of the Pokémon and often change its types and ability as well.

// image

When I first put mega evolutions into [PokémonCompDB](/pokemoncompdb.html), I made them their own feature. Mega evolutions were recognized by the application and when the user gave a given Pokémon set the correct mega stone, the type and visual information updated to show the mega form. I realized some time later that mega evolutions are actually just a variant of form changes, which I've talked about quite a bit before.

The things that caught me out about mega evolutions were, inevitably, *almost* all of them work the same way. You give a Blastoise a Blastoisinite and it can turn into Mega Blastoise during battle. But there are a couple of legendary exceptions that have mega evolutions that act a bit different:

| Rayquaza | Groudon | Kyogre |
|:--------:|:-------:|:------:|

Unlike all other mega evolutions, Rayquaza can mega evolve as long as it knows the move Dragon Ascent (which only it can learn). This means that PokémonCompDB now needed to be aware that changes to the moves known by a given set may cause mega evolutions to become available (and likewise removing a move may remove the availability of a mega evolution).

// mega rayquaza image

When I generalized mega evolutions into forms, Rayquaza turned out to not be the only instance of this kind of form change. [Meloetta](https://www.serebii.net/pokedex-sm/648.shtml) changes between its Aria and Pirouette forms (during battle and everything) based on whether it knows [Relic Song](https://www.serebii.net/attackdex-sm/relicsong.shtml), which is an exact analogue for Rayquaza's mega evolution behavior.

Next up are Groudon and Kyogre, which are different to other mega evolutions in the same way as one another. There's certainly a canonical argument that Groudon and Kyogre are not undergoing mega evolution at all, but instead "Primal Reversion", which is a special kind of form change. I chose to add them in when adding mega evolutions, since Omega Ruby and Alpha Sapphire put these forms front and center, at the time I felt leaving them out wasn't sensible. Similar to mega evolutions, the primal reversions include type changes (in Groudon's case adding the Fire type) and stat boosts.

| Primal Groudon | Primal Kyogre |
|:--------------:|:-------------:|

Groudon and Kyogre become Primal Groudon and Primal Kyogre while holding the Red Orb or Blue Orb, respectively. Unlike mega evolutions, these primal reversions happen *as soon as they are given the item*. So you see Primal Groudon in your party on the pause screen, but you never see Mega Rayquaza, because *normal* Rayquaza is the one you carry around with you, it just transforms during battle.

Since normal mega evolution Pokémon go into battle in their non-mega-evolved form, PokémonCompDB displays their non-mega ability as well. That's because it may be important to your strategy that the original ability is active when the Pokémon is first used. Take Salamence for example, who has Intimidate as its non-mega ability, which will activate as soon as Salamence is sent out and then doesn't do anything more (from a competitive battling point of view). But you can then mega evolve Salamence and take advantage of Mega Salamence's Aerilate ability for the remainder of the battle.

But in Groudon and Kyogre's case, they're already transformed when the battle starts. So Groudon's Drought and Kyogre's Drizzle don't come into play (instead it's Primal Groudon's Desolate Land and Primal Kyogre's Primordial Sea). PokémonCompDB displays this distinction by *not* displaying the non-mega ability in this case.

And again, like Rayquaza, when I generalized mega evolutions to support all form changes, I found another Pokémon, Giratina, that behaves very similarly! Giratina changes into its Origin form while holding a Griseous Orb, very similarly to how Groudon and Kyogre change form.

// image

I'm continually impressed by how the Pokémon data set rewards "correctness" in this way. I keep finding new variants of form changes and Pokémon behavior the longer I work on PokémonCompDB, but I also often find other Pokémon that I hadn't considered fit very well into new boxes that I come up with to classify those changes!