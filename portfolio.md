---
layout: page
title: Portfolio
permalink: /portfolio/
date: 2015-11-14 19:14:00 -8000
---

This page covers my work history and side projects in more depth, with pictures.

* [Roblox](#roblox)
* [Munkyfun](#munkyfun)
* [5th Planet Games](#5pg)
	* [Dawn of the Dragons](#dotd)
	* [Legacy of a Thousand Suns](#lots)
	* [Clash of the Dragons](#cotd)
* [J.A.G.S Home-brew Game System](#jags)
* ["Spaceships"](#spaceships)
* ["Dark Mod" &mdash; Minecraft 1.6/1.7 Mod](#darkmod)

<h2 id="roblox">Roblox</h2>

I work at Roblox now. I'm a Senior Engineer on the physics engine team.

<h2 id="munkyfun">MunkyFun</h2>
At [MunkyFun](http://www.munkyfun.com/) I did front-end mobile development (mostly in Unity) for [League of War: Mercenaries](http://leagueofwarmercenaries.com/). 

<iframe width="640" height="360" src="https://www.youtube.com/embed/YJTc845YYRM" frameborder="0" allowfullscreen></iframe>

I did a lot of work on architecture, UI systems, data management, and gameplay programming. 

In gameplay I wrote a lot of the code for the PvE campaign, crafting, localization, and unit progression.

I'm proud of my work writing and maintaining one of the most used systems that controls the flow through all the different screens of the game and manages scene loading. It has a small type safe API, and it's almost impossible to use incorrectly. People don't hate it (anymore)!

I write a lot of tools, utilities, and documentation to make dealing with some of the more esoteric behaviors of Unity simpler and more clear.

<h2 id="5pg">5th Planet Games</h2>

I joined [5th Planet Games](http://www.5thplanetgames.com/), as an intern right after they incorporated in 2009. I had a huge technical role in the conception, release, growth, and ongoing maintenance of _Dawn of the Dragons_, _Legacy of a Thousand Suns_, and _Clash of the Dragons_.

I was the second engineer to join the company (after the CEO himself), and worked on every layer of every stack there. With most features I was in charge of implementing them full stack, end to end, client presentation to server to SQL queries.

The games had to scale to handle an average of around 100,000 MAU and 20,000 DAU at their peak. All clients (HTML, Flash) connected to Java based socket servers backed by MySQL databases.

I labored to set standards and best practices: I wrote the code style guides, set up version control and trained the devs for it, wrote build scripts, set up continuous integration and deployment systems. I wrote tools to automate the asset pipeline, and scripted bandwidth (and money) saving asset compression and optimization. I documented best practices. I interviewed, on-boarded, and trained other engineers.

Later I worked with the team to improve security practices in all the company's projects. I fixed existing exploits, and preemptively fixed numerous yet unobserved ones related to trust issues and inconsistent enforcement of privileges; exploits that could have allowed malicious clients to embed arbitrary images and flash apps in global chat, or let anybody disband any guild.

[dotd]: http://www.dawnofthedragons.com/ "Dawn of the Dragons"
[lots]: http://www.legacyofathousandsuns.com/ "Legacy of a Thousand Suns"
[cotd]: http://www.clashofthedragons.com/ "Clash of the Dragons"

<h3 id="dotd">Dawn of the Dragons</h3>

[_Dawn_][dotd] was the company's first game and helped the company achieve profitability. It's a fantasy-themed quest list based game in the ilk of Castle Age and Mafia Wars.

It's unique characteristics are it's original raid system, with small groups, guilds, or even the entire player base globally fighting the same bosses together (which competitors later copied); and the story and lore, all written by a UK based professional writer.

Some of the most visible items I built or overhauled are the Profile, Quest, and Crafting pages; as well as some underlying components like analytics, and runtime asset loading and caching.

![Dawn quest page](/images/portfolio/dotd_quest.png)
![Dawn craft page](/images/portfolio/dotd_craft.png)

<h3 id="lots">Legacy of a Thousand Suns</h3>

[_Legacy_][lots] was the company's second game, a "reskin" of _Dawn_, collaborating with art contractor [Concept Art House](http://www.conceptarthouse.com/) on art and style. 

It's base, _Dawn_, was the company's rushed first game. I worked under *very* tight deadlines leading the project to overhaul the client-side codebase, refactoring the _Dawn_ codebase to create MVC separation, fixing bugs, and working tightly with artists and designers to implement their design changes and new features with lightning turnaround.

Post-release, I did the design and technical work to implement localization, which we back-port to _Dawn_ and reused as-is in _Clash_.

![Legacy mission page](/images/portfolio/lots_mission.png)
![Legacy profile page](/images/portfolio/lots_profile.png)

<h3 id="cotd">Clash of the Dragons</h3>

[_Clash_][cotd] is a digital collectible card game, collaborating with To Be Continued LLC (Later 5th Planet East). I most visibly worked on card display in general, and the deck editor system from end to end; which remains entirely functionally unchanged, despite the game going through multiple UI overhauls since my departure.

![Clash deck editor](/images/portfolio/cotd_deck.png)
![Clash gameplay](/images/portfolio/cotd_game.png)


<h2 id="jags">J.A.G.S Home-brew Game System</h2>

Originally an honors project for Assembly Programming, and later Microcontroller C Programming at Sierra College; I designed a small handheld game system from scratch.

I drew the schematics, laid out, and hand routed (no auto-router I could afford could) the boards in Eagle CAD. I had a handful of boards manufactured, and hand soldered and tested a working model. It included an ARM 7 microcontroller, a vibration motor, accelerometer, an analog control stick, 3 face buttons, and 2 rear buttons. The white strip is a connector for an LCD screen, which I didn't finish the drivers for before all my time was being used at 5th Planet; I was able to test everything else on the board, though.

Special thanks to Sierra College instructor Mike Dobeck for offering the honors project and [Line 6](http://line6.com/) Senior Wireless Engineer Jim Purcell who generously spent much time critiquing my work, and donated use of numerous components and tools.

![JAGS final](/images/portfolio/jags_test.jpg)
[![Schematic](/images/portfolio/jags_schematic.png)](/data/portfolio/JAGS.pdf)
[![PCB layout](/images/portfolio/jags_top.png)](/data/portfolio/JAGS_TOP.pdf)
[![PCB layout](/images/portfolio/jags_bottom.png)](/data/portfolio/JAGS_BOTTOM.pdf)

<h2 id="spaceships">"Spaceships"</h2>

Ongoing side project collaborating with friend and former 5th Planet co-worker, Ian Green.

"Spaceships" is a simple multi-player top-down space shooter. The movement in particular has been particularly well refined.

The client was originally written in Flash, with an authoritative server in Java using Netty for communication over a custom binary protocol. In this version you could fly around with other people and shoot bullets at each other.  Although the game was originally designed so that the client and server would not need to share much logic, as the game evolved it unsurprisingly became necessary to do so.

To unify the client and server codebase under one platform, and escape liscencing changes to Flash that would have required a 30% royalty from this game, we ported our work over to Unity and added 3D art. The Unity version had movement and multiplayer support after a couple days work. Now you can shoot lasers and missiles at your friends and dummy target drones that wander around the map.

Textures and level parts were done by Ian Green. Ship model made by [Brent Douglass](http://bdouglass.weebly.com/)

![Spacships Unity](/images/portfolio/ss_unity.png)
![Spaceships Flash](/images/portfolio/ss_flash.png)

<h2 id="darkmod">"Dark Mod"</h2>

Dark Mod is a mod for the PC (Java) version of Minecraft.

I played a lot of Minecraft with my friends. There were some things we wished existed for the game that didn't, or didn't work well in existing mods. My Java was strong, so me and my friend Ian Green (game designer by trade) started a mod.

I set up the tools and set up code for custom oriented blocks and armor. I implemented paintable Pots, that work like smaller chests that you can relocate with contents in tact, paint, and name.  The lids lift open facing you when you look inside them.

I haven't had time to to work on Dark Mod much lately, but Ian's been using it to learn Java, and has implemented a lot of charming, novel features himself that add a lot to the game. [He's written more in depth about it on his site.](http://test-igdv.rhcloud.com/mcmod) There's more pictures there too.

![Dark Mod Pots](/images/portfolio/mcmod_pots.png)
![Dark Mod Main](/images/portfolio/mcmod_main.png)
![Dark Mod Combat](/images/portfolio/mcmod_combat.png)

<style>.dsq-brlink, #disqus_thread { display: none; }</style>