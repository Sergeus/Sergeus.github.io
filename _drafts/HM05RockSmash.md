---
title: HM05 Rock Smash and TM94 Secret Power
inline_title: true
---

// mention Dive

When working to support the newly released Pokémon Sun & Moon <sup>(6 months after they came out)</sup> there were a lot of new concepts for me to wrestle with to represent the new mechanics [Game Freak](https://en.wikipedia.org/wiki/Game_Freak) added in Generation 7. Things like [Alolan forms](https://bulbapedia.bulbagarden.net/wiki/Regional_variant) and [Z-Moves](https://bulbapedia.bulbagarden.net/wiki/Z-Move) were the visible, big ticket items, but I ran into an unexpected little problem with two TMHMs.

To understand this post, I'll give you a brief bit of context about [TMs and HMs](https://bulbapedia.bulbagarden.net/wiki/TM) in Pokémon. TMs (Technical Machines) and HMs (Hidden Machines) are items in the Pokémon games that teach one of your Pokémon a certain move. They're numbered to indicate which move they teach. In Sun & Moon, TM13 teaches [Ice Beam](https://www.serebii.net/attackdex-sm/icebeam.shtml), for example. 

Originally there were two differences between TMs and HMs: 

* TMs were single-use and HMs were not
* HMs could be used in the Pokémon overworld to traverse obstacles ([Surf](https://www.serebii.net/attackdex-xy/surf.shtml) across water, for example) once you had the right [gym badge](https://bulbapedia.bulbagarden.net/wiki/Badge). 

As of Generation 5 (Black & White and Black 2 & White 2), TMs became multi-use. And in Generation 7 (Sun & Moon) HMs were retired in favor of [rideable Pokémon](https://bulbapedia.bulbagarden.net/wiki/Pok%C3%A9_Ride). It remains to be seen if that change is permanent, but I prefer the rideable Pokémon a lot.

![](/assets/img/tmhms.png)
*TMs and HMs. Color coded and everything.*

Like I mentioned in [my last post]({% post_url 2017-10-13-BonslyLucarioAndVaporeonInGeneration5 %}), in each Pokémon game starting from Ruby & Sapphire (Generation 3) you have the ability to port your monsters over from the older games. This introduces loads of unique move combinations for Pokémon that used to learn certain moves in older games, but don't any more.

Sun & Moon is no exception, so Pokémon are free to be imported over from Generation 6 (X & Y and Omega Ruby & Alpha Sapphire).

A lot of Pokémon no longer learned moves in Generation 7 that they did in Generation 6 by TM or HM. That was fine - I'd already dealt with that kind of imported difference when I worked on Generation 6's database.

However, Omega Ruby and Alpha Sapphire, as their names suggest, are remakes of Ruby and Sapphire. Game Freak did change the TMs in them - so the TMs and HMs in Omega Ruby & Alpha Sapphire were much like the ones in X & Y, rather than being like the original Ruby & Sapphire.

I say "much like," not "the same". [Rock Smash](https://www.serebii.net/attackdex/rocksmash.shtml) was a HM in the original Ruby & Sapphire, but remained a TM in all of the games since, including X & Y. Game Freak elected to return Rock Smash to its HM status in Omega Ruby & Alpha Sapphire, which meant that Generation 6 was the first one I'd run into that *didn't* have the same TMHM numbering across the whole thing. So things predictably didn't work.

![](/assets/img/smashable-rock.jpg)
*A smashable rock in Pokémon Omega Ruby.*

The reasons for this are fairly obvious - HMs can be used in the overworld and the mechanics of using Rock Smash remained in Omega Ruby & Alpha Sapphire. So it had to stay as a HM.

In X & Y, Rock Smash was TM94, but in Omega Ruby & Alpha Sapphire it became HM05. And just for kicks, the move [Secret Power](https://www.serebii.net/attackdex-xy/secretpower.shtml), which was used for the Omega Ruby & Alpha Sapphire exclusive-mechanic of [secret bases](https://www.serebii.net/omegarubyalphasapphire/secretbaselocations.shtml), was not available as a TM in X & Y. So Omega Ruby & Alpha Sapphire *replaced* the now-missing TM94 of Rock Smash, with Secret Power. So the same TM number didn't even mean the same thing across that generation!

I can only assume Game Freak did that to keep the TM numbers contiguous. (And before you ask, Secret Power was TM43 in the original Ruby & Sapphire.)

![](/assets/img/nigel-thornberry.jpg)
*I would be lying if I said this joke wasn't part of why I wrote this post.*

Today's tidbit was fairly straightforward, and many of you readers probably noticed this change while playing the games. What tripped me up here was the way it made Generation 6 subtly inconsistent from all of the previous ones.