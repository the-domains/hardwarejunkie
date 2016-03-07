---
inFeed: false
hasPage: true
inNav: false
inLanguage: null
starred: false
keywords: []
description: ''
datePublished: '2016-03-07T20:03:02.423Z'
dateModified: '2016-03-07T20:01:06.004Z'
title: Overclocking an Outdated (but relevant) Graphics Card
author: []
sourcePath: _posts/2016-03-07-overclocking-an-outdated-but-relevant-graphics-card.md
published: true
authors: []
publisher:
  name: null
  domain: null
  url: null
  favicon: null
url: overclocking-an-outdated-but-relevant-graphics-card/index.html
_type: Blurb

---
# Overclocking an Outdated (but relevant) Graphics Card

So my daily driver is a fairly powerful but somewhat dated rig ; it runs on an i7-4790, XFX R7950, and 16GB RAM in a Corsair Air 540\.  I use it for all of my daily workflow in my business, including accounting, invoicing, document creation, web design, light illustrator work, and of course the occasional gaming during downtime.  It runs four 24″ Acer 1080p monitors so I can multitask better game while working.  Aside from the motherboard, CPU, and Samsung SSD, all of the components are two years or older.  The GPU specifically has been in service since August of 2013\.
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/8ca10768-88da-4d9a-a03f-3b8305693173.png)

_The Speccy report for my daily driver PC that I am performing this testing on._

This machine is used daily to run my business, so it needs to be stable above all else.  For this reason, the stock non-k CPU is cooled by a [Corsair H110i GT][0]. The 7950 from XFX however, runs the company's stock 'GHOST' air cooler ([here is it's listing on Amazon][1], though it is no longer stocked).  I decided it would be worth some tinkering to see what kind of performance I could pull out of it bone stock, specifically for my current favorite time waster, Shadows of Mordor.

I normally run this game at 1080p native, in borderless mode, locked to 60 FPS with VSync on.  I turn tessellation and AA off, and crank everything else.  The game looks great to me and runs smoothly, but I do still get the occasional dip into the 40 FPS range when there's a ton of stuff going on.   This makes the fighting stutter for a brief moment, throwing me off of my rhythm, and ending up with my character taking a hit or two he shouldn't have.

In the name of science, frustration, and tinker curiosity, I decided to see what I could do to push the card a wee bit farther and eliminate the occasional issues I was having.

As a disclaimer, I have overclocked a few CPUs (not since the AMD Athlon era), but have never done so with a GPU.  I headed over to the[trusty reddit overclocking sub][2], and pulled up the /r/overclocking[General GPU Overclocking Guide][3]maintained by the fantastic folks of that sub.  The first things it recommends are to verify your PSU will handle the extra load (I have a Thermaltake 750W unit, so I should be fine) and to obtain both overclocking software and a good benchmark/stresstest.

For simplicity's sake, I made the decision to stick with the basic Catalyst Overdrive utility, and Shadows of Mordor's built-in benchmark utility.
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/490721ff-3c4c-4ceb-972c-058198bf146d.png)

_The AMD Catalyst Overdrive Utility_

I decided to run 3 laps of the built-in SoM benchmark at each step to get a better idea of consistent average FPS numbers, and to stress the card a bit harder to push that inevitable crash out.  I also gave the whole system ten minutes between runs to cool back down to idle temps.  For these tests, I turned off the framerate lock and VSync, but left all other graphic settings the same.  I ran a baseline pass (three back-to-back benchmarks) at the stock core clock of 900MHz and the stock memory clock of 1300MHz, changing only the power control setting to +20 (max).  My baseline average framerate was 62.13 FPS.

This is quite respectable, especially with all the eye candy turned up, but I wanted to see if I could push it higher to smooth out the occasional dips in actual gameplay.  I ended up running 12 additional passes (13 total) following the theory of the reddit guide.  My initial overclock was 5% of base core clock (45MHz), and I bumped ~15MHz each pass after that until crash, then dialed back 10MHZ until stable.  I then moved to memory clock, and repeated the procedure up in 25MHz increments, then down 10MHz at a time.  For those that just want to see the results, here's the chart:
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/f14d33cf-608d-4aa3-86b9-961f260648fb.png)

_Pass 1 was the stock baseline, represented as 100%. Subsequent passes are percentages of these numbers._

And here is the raw data collected in Excel whilst testing, that the graph is built from:
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/c82fe4f7-3f9a-4a9e-b9b9-fcf016cbf2bc.png)

_Raw Excel Data from chart above, plus extra information collected._

As you can see, we actually achieved a decent stable overclock, resulting in about a 14% increase in average frame rate (62.13 to 70.68).  The core clock capped out at 1020, a 120MHz or 13% overclock from stock.  The memory clock only made it up 40MHz to 1340, or a 3% overclock.

I then spent some time with Kombustor and ran several stress tests between 10 and 30 minutes, and the card held remarkably stable at the final numbers of 1020 core and 1340 memory.  Temperatures remained as sane as one would expect with an older, tired air cooler -- around 82 degrees.  The fan, still set to auto in Overdrive, never passed 70%, even after an hour of constant stress testing.

Some may say it is possible to be a bit more aggressive with my fan curve , and that I could have gotten temps down and pushed the card a bit more.  However, with the loud, dual fan GHOST cooler in my Corsair AIR 540, anything past the 70% mark moved my system firmly into hairdryer sound levels.
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/d12a1a26-e0b4-4b84-803e-512a39726034.jpg)

_Is it a hair dryer or a video card? Blind people may not be able to tell....._

These numbers may not _seem _very exciting, and they really aren't from an  "OMG massive performance" standpoint, but this exercise was more for a 'quality of life' improvement than raw performance.  With the extra headroom the otherwise dated card now has in this game, the playability of the game has increased noticeably.  As I do more and more pieces on this site, this will be a consistent theme.   I do this more for the fun factor and the everyday usability gained rather than having larger bars on my graphs than everyone else.  Also, it gives me an excuse to be sitting in front of the computer 'working' when the missus needs me for something.

Down the road I may revisit this and see what else I can do to gain a bit more performance.  Let me know in the comments if you have any thoughts, or comment on these ideas I am tossing around:

* Replacement of the thermal pads/paste (as stated above, the card has been in service since 2013) as well as cleaning out what may be significant dust in the cooling system.  This should bring down temps, but will that translate to stability at a higher overclock?
* Removal of the other three monitors in my quad setup to allow the GPU to focus on the game
* Running fullscreen rather than borderless
* Anything else I can come up with in the interim!

Thanks for reading through my drivel, and feel free to subscribe to the blog, [my Facebook page][4], or leave a comment and interact with us!

[0]: http://amzn.to/1QClVIG
[1]: http://amzn.to/1Layo6n
[2]: https://www.reddit.com/r/overclocking
[3]: https://www.reddit.com/r/overclocking/wiki/gpu/general
[4]: https://www.facebook.com/hardwaretinker/