---
layout: post
title: How Adobe Murdered Flash
date: 2016-04-25 00:26:00 -0800
redirect_from: /how-adobe-murdered-flash/
---

Flash has been dead for a while. I moved on a long time ago, but back in it's day I was a happy specialist in AS3 development. Flash used to be something special.

In it's heyday Flash had a lot going for it. Unparalleled reach, a solid runtime, a compact file format, great documentation, and most importantly: *a thriving community*. 

And then one day, almost overnight, there wasn't. Within a couple months, everyone was gone. Everyone. Everyone stopped talking about it, even the most enthusiastic Adobe employees stopped blogging about it on their personal blogs. Try to find an AS3 based library project that was still in active development after mid 2012. You won't. It was not a slow death. You'll notice a marked consistency in when they stalled.

HTML5 didn't kill Flash based on merit. That would've taken much longer. It wasn't ready. It still isn't. I cringe when people say this.

Adobe murdered it.

## Imagine... ##
Imagine you're a high-end web dev in 2017 working on some fantastic new experience that uses WebGL and typed arrays, features that have been out for a while. Imagine it all works consistently on 95% of browsers, and  the same code compiled natively for mobile. I know it's hard to picture with a web stack, just try.

Suddenly W3C announces whenever you use WebGL and typed arrays together, they demand a 30% royalty on all revenue you make on any app you make involving javascript that uses those features. Hypothetically, there is actually a sane way they can enforce this.

Screw that. Time to start over, get a new set of cross platform tech?

That was Flash in 2012.

In march 2012, Adobe announced ["Premium Features for Gaming"](http://blogs.adobe.com/flashplayer/2012/03/adobe-introduces-premium-features-for-gaming-with-flash-player-11-2-announces-collaboration-with-unity-technologies-2.html), a 30% royalty for flash apps that used Stage3D (like WebGL, with better fallbacks), and some optimized memory access instructions. Both features had already been publicly available for months prior to this announcement and people had written games and libraries around them. There were large projects still in development build around them.

3 months later they all-too-quietly reversed the royalty, but by then everyone had quit their AS3 development jobs and moved on to other platforms. Adobe made no effort to publicize the reversal and no one was looking back. We never heard about the recently hyped [Unreal Engine 3 support for Flash](https://www.unrealengine.com/news/epic-games-announces-unreal-engine-3-support-for-adobe-flash-player/) again. I'd already ported my game projects away. And nobody trusted Adobe as a platform company ever again.

## Thanks, Adobe ##

It's a story worth knowing, because it's a good lesson in how a critical developer community trust violation killed a platform's future overnight. 

It was a clear move trying to copy the likes of Apple's App Store and Steam, a ballsy move to monetize their impressive market share. The difference there is those platforms offer a market place, distribution, and visibility in exchange for their cut; they provided a service. It helped that those terms were clear from when from when you would be first considering targeting those platforms.

Adobe had no market place ready. They had no services to offer in exchange. They were simply *allowing* you to use thin OpenGL bindings and some raw byte arrays, and suddenly expecting a publisher's share while you were still on the hook for any costs of publishing and distributing your app or game.

If they had announced this royalty when they first announced Stage3D it might have been fine. We could have evaluated to use these features with full knowledge of what we were getting in to. It might have been worth it? Or more likely everyone would have avoided these features early on. Instead, they waited until everyone was addicted to using them before surprise announcing their insane cost.

I assume the rug pull wasn't orchestrated in advanced and that this was more of a case of manslaughter or reckless endangerment than first degree homicide. Maybe Flash wasn't profitable enough for the executives behind this stunt to care if it killed the platform or not? Still tragic. 

It's funny to consider some of the criticisms about bloat and performance people heaped on it then, [considering the state of modern javascript apps](http://product.voxmedia.com/2015/5/6/8561867/declaring-performance-bankruptcy). Some of the UX is better these days (linking in flash apps were awful), and maybe someday javascript capabilities will catch up (we can dream), but there are some experiences that I haven't seen replicated since. If anything comes close, it's broken on some browser or devices that Flash covered well. The potential and accessibility were really unparalleled, even now. Terrible web based apps have proven to be just as terrible as terrible Flash apps. Something of value was lost. I would have taken an AIR based app development future over the Electron hell we live in now. Alas.

I'm in a better place now, but wish I could say the same for the web. Whenever I have to do web dev or cross platform development even now, I still shed some tear for Flash. RIP.