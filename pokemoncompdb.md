---
title: PokémonCompDB
---

Throughout this blog, you'll probably see my application, PokémonCompDB, referenced. I'll often link to this page when it comes up for the first time in any given post. Here, you'll find some more in depth information about what the application is, what it does, how and why I made it, and some other information I thought might be useful.

# What is PokémonCompDB?

PokémonCompDB (predictably short for Pokémon Competitive Database) is an application I've been working on as a hobby project. It's an application for keeping track of competitive Pokémon teams.

It's a little web server that runs locally on a Windows PC and you can interact with through a browser.

### It looks a bit like this (click to view full size):

[![A bunch of my competitive Pokémon teams](/assets/img/pokemoncompdb-team-preview.PNG "A bunch of my competitive Pokémon teams")](/assets/img/pokemoncompdb-team-preview.PNG){:target="_blank"}

### And this:

[![The summary page for my competitive Charizard](/assets/img/pokemoncompdb-charizard-summary.PNG "The summary page for my competitive Charizard")](/assets/img/pokemoncompdb-charizard-summary.PNG){:target="_blank"}

If you're not familiar with competitive battling, there are a lot of statistics about what makes a Pokémon good at battling. The games don't actually show you a lot of that information, though you can keep track of it manually. This application lets you record that information in a system that understands what you're doing. It can make recommendations and make sure you don't accidentally note down incorrect information.

If you are familiar with competitive battling, PokémonCompDB lets you track, among other things: 

* Move sets
* Items
* EVs and IVs
* Natures
* Your current EV training progress

It makes recommendations of how you should teach a Pokémon your selected move set based on which game you tell it you're playing. It lets you group sets into teams so that you don't forget who goes with who. And a variety of other things! My objective was to make the "summary" page for a set to be a one-stop-shop for all of the information you need to train that Pokémon in any of the games.

# Where can I get it?

You can't, unfortunately! At the moment it's just for my use. I'll need to talk to several fan sites about using their data before I could release it in any form.

# Why did you make it?

I play competitive Pokémon on the official game cartridges, instead of one of the popular simulators that are available online. The simulators are awesome and make it a breeze to create new teams and iterate on making them better.

I find I enjoy battling more on the official hardware and online on Nintendo's WiFi tournaments, even though that involves a lot more work in actually creating your teams.

Without going into the nitty-gritty of competitive battling, there are a lot of statistics about Pokémon and what makes them better at battling that the games don't display to the player. (Though the newer games have been making more of this information available over time!)

These hidden statistics can be derived from your gameplay. For example, you can choose to defeat certain opponents and accrue what the community call EVs, which raise your Pokémon's stats. So it's up to you to keep track of all of the sets that you've designed for your team. To know which items they should be holding. To know which moves they should be learning. And working out how they learn all of those moves often involves consulting several different fan websites to pull together the information you need!

For the longest time, I kept track of my teams with a big Excel document. That worked for a while, but Excel obviously knows nothing about Pokémon, so it's difficult to make that spreadsheet make intelligent associations that are to do with the game's rules. (Not impossible - Excel can be used for serious wizardry - but more complicated than I wanted to deal with.)

And from that, came PokémonCompDB! I'm a game developer, more specifically a tools programmer, so I have practice at building applications like this. I had very limited exposure to web technologies, so I decided to make a dual exercise of this: I'd create an application to keep track of my competitive Pokémon teams and learn more about web applications in the process by making it a local web server that you interacted with through your browser.

It's been very successful on both counts!

# How did you make it?

This is one for you technical folks!

The local web server is written in C#, using a lightweight web server framework called [NancyFx](http://nancyfx.org/).

The database of information about the games stored as an SQL database, using [SQLite](https://www.sqlite.org/). It was previously an enormous JSON file that none of my text editors could open, but I changed that up in April of 2017. (Most text editors do not like 80MB of json that's all on one line.)

The web interface is written in HTML, JavaScript, and CSS. I use [Bootstrap](http://getbootstrap.com/) for layout styling and [JQuery](https://jquery.com/) for a lot of the interactive behavior. I use [SSVE (The Super Simple View Engine)](https://github.com/NancyFx/Nancy/wiki/The-Super-Simple-View-Engine), which comes packaged with NancyFx, as the templating engine for the pages.

I also use some other JavaScript and JQuery plug-ins, such as:

* [JQuery.UI](https://jqueryui.com/) for some of its interface components
* [JEditable](https://appelsiini.net/projects/jeditable/) for all the click-to-edit goodness
* [JQuery.AreYouSure](https://github.com/codedance/jquery.AreYouSure) to make sure I don't accidentally discard a partially created set

I also wrote a command line application for parsing a variety of Pokémon fan sites to generate the SQL database. I'll go into more detail on that below, but in terms of dependencies, the parser is written in C# and uses [HtmlAgilityPack](https://www.nuget.org/packages/HtmlAgilityPack/).

I use [Git](https://git-scm.com/) for source control. And a [GitLab](https://about.gitlab.com/) instance hosted on my home server as a source control server and feature/issue tracker.

I also did a fair amount of chopping and changing in [GIMP](https://www.gimp.org/), the image-editing tool (a free alternative to PhotoShop). Mostly coercing images from different sources into consistent sizes, creating some simple icons, and other such straightforward image editing requirements for any project that deals with a significant quantity of images from other sources.

# Where did you get the Pokémon game data?

You might be wondering *how* I got an SQL representation of the data from the Pokémon games in a format that my application understands. Those kind of data sets aren't just lying around on the internet in such convenient formats.

This is where the dedicated work of a bunch of fans has helped me out a lot. I wrote a command line application to parse the web pages from some fan sites and collect the data I need.

The lion's share comes from [Serebii.net](https://www.serebii.net). I've discussed PokémonCompDB briefly with Serebii's awesome site admin to get his blessing to use their data. (As long as I credit them of course, which is right here! And at the bottom of every page of this blog!)

But there are a few other sources for some specific info. They're all listed here:

* [Serebii](https://www.serebii.net) for Pokémon move learning data (by far the most complex part of this data set), form data for all of the different species, Pokéball data, EVs earned from defeating species, and more
* [Smogon](http://www.smogon.com/) for the initial seed of the list of Pokémon species, and the master lists of items, moves, and abilities
* [Bulbapedia](https://bulbapedia.bulbagarden.net/wiki/Main_Page) for Pokédex numbers, egg groups, and location data (to let PokémonCompDB calculate the best locations to recommend for EV training)
* [PkParaiso](https://www.pkparaiso.com/) for the animated 3D model gifs
* [CodeNamePlayer on DeviantArt](http://codenameplayer.deviantart.com/art/Pokemon-XY-Menu-Icon-Sprites-411129707) for sprites for all of the Pokémon up to Generation 6 (X&Y)
* [The PokeSprite project](https://github.com/msikma/pokesprite) for sprites for the Arceus and Genesect non-standard forms

The parser also contains a lot of custom workarounds discovered individually by me while developing it, when my application didn't reflect the games in some way that I hadn't expected. PokémonCompDB also represents a lot of information that isn't consistently described on many fan sites.

I can regenerate the database for any given generation (currently only 6 and 7 are supported) by rerunning the parser against a downloaded copy of the relevant pages from the fan sites.