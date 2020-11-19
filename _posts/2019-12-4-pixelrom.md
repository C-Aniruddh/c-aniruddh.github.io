---
layout: post
title:  "PixelROM and FlexOS - Custom firmwares based on Android"
author: aniruddh
categories: [ Firmware Development ]
image: https://aniruddh-chandratre-e877.netlify.app/static/c37dea6b0bedfa14c471216c329d5dc2/a41d1/wpid-wp-1433613089114.jpg
toc: true
---

## Introduction
PixelROM and FlexOS were custom android firmwares designed to provide a customisable, secure and up-to-date firmware that can be installed on any supported device. PixelROM was started back in late 2013, and it was mid 2014 until it made any public releases. PixelROM and FlexOS was started by two of us, me and Arnav Gosain. At the time of launch, I was 15 years old and Arnav was 13. As soon as PixelROM was released,it gained worldwide popularity and the Google+ community started growing. When Android Lollipop was announced, the core team decided to re-brand as FlexOS.

With the release of FlexOS, we grew to a team of 40 members globally including the core team, designers, device maintainers, etc. FlexOS quickly got popular and was labelled as one of the best ROMs available in the market. Both, PixelROM and FlexOS were completely open source and could be compiled and distributed by anyone.

<iframe width="560" height="315" src="https://www.youtube.com/embed/W8Ig1AgeQEQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

There are a few things we kept in mind when designing both the firmwares!

## Focus on important parts of the OS

Keeping it simple!

### Smoothness and performance

Let’s immediately start off with one of the most important things that is evaluated in the first hours of flashing a new ROM: smoothness and performance. Being based on a smooth and stable source code does not automatically makes the custom version just as smooth. The FlexOS team was filled with kernel developers, designers and user experience experts. This enabled the Flex Team to provide an intuitive and almost flawless experience to anyone who opted for it.

One custom firmware review [website](http://www.androidscout.com/android-rom-list/flexos/tiago-marques-review/) says the following :

> FlexOS is another wolf on the pack of CM open source code based ROM and anybody that tried the latest CM12.1 knows that smoothness and snappiness are two things those nightly builds achieve. Being based on a smooth and stable source code does not automatically makes the custom version just as smooth but it didn’t come as surprise that FlexOS is, indeed, very smooth. Every animation and every transition is done without any visible lag. Even on heavy multitasking between apps like Youtube, Chrome, writing emails, office apps and throwing gaming to the mixture there is no noticeable lag on any animation. Of course, the good specs of the Oneplus One plays an important part in this but I did flash ROM’s where I could see some drop in frames on heavy usage. Not on FlexOS so rest assure that it will get the job done, no matter what you throw at it (as long as the hardware can withstand those tasks).

> But be aware that what I observe (and as the vast majority observed with FlexOS) could not be the same for you as the GAPPS package that you use or even the process of flashing can play an important role on final performance. But the vast majority of FlexOS users don’t have any performance issues so, statistically speaking, there is a high chance that you won’t encounter any problem regarding smoothness.

> I’m very reluctant talking about benchmarks as from my experience they don’t always correlate with my daily usage. For example, some phones with Mediatek chips can achieve high scores on benchmarks but on daily usage you can observe high frame drops across the entire system. Nonetheless, it’s at least relevant to mention the scores Oneplus One can achieve on FlexOS. On Antutu it scores around 46000 and on Geekbench 3 it scores around 1ooo and 31oo on single-core and multi-core respectively.

> The version tested was a nightly build (2015-05-22) based on android 5.1.1, running everything stock out of the box. No Xposed and no custom kernel, everything as the developers and Flex community released this version. Speaking of that, they have a very good community behind Flex (can be found on Google+ FlexOS) , always willing to help out struggling flashaholics and use the community feedback for future builds. That for me is always a very BIG plus that I gladly take. Keep those coming!

### Battery Life

We, as developers of the firmware, took special care of all the ways battery drains could occur. On the kernel side, we shipped kernels with special governors and additional tweaks to get the sweet spot between performance and battery savers. The FlexControl application allowed the user to select the mode, balanced, battery saver or performance depending on what they're about to do. One of the very unpredictable battery drain issues is caused by apps which are causing wake locks. FlexOS took special care of this by having a WakeLock manager built right into the ROM. This way, the user can know which application is not letting the phone into Doze mode and what further steps should be taken for preventing battery drain!

The same review website says :

>Right after overall performance comes the second biggest asset we always look for on “freshly” flashed ROM and that is battery life. Do a quick search on forums and you will find users asking “what’s the better ROM for battery life?” or “what can I do to improve my battery performance?”. They put battery life on top of any other ROM feature and that’s perfectly understandable, I mean, what’s good about having outstanding performance if our machine can’t even last a full day? My evaluation of FlexOS was based on pure stock ROM, no custom kernel and no custom tweaking like undervolting. Besides, why would I want a high-end CPU to have it limited but that’s my take on this subject.

>Normally, my day is spent with WiFi and 4G constantly on with a lot of constant sync on the background. On my daily commute my data connection keeps bouncing between 4G, 3G and H+ since I don’t get full 4G coverage from where I live. And we know the negative impact on battery when the signal is not stable. On my phone I tend not to game much (occasionally Limbo and Monument Valley) and mostly is spent web browsing, social media, media consumption (mainly music) and occasional photography. I use almost every Google apps (call me crazy, I know!), “juice hungry” Facebook and Messenger, Hangouts, etc and to keep those wakelocks in check I use Wakelock Detector to identify who’s draining my battery and Servicely to block them. Furthermore, I have the “Adaptive brightness” and “LiveDisplay” on, as well as Double-tap to wake/sleep and accidental wake-up. Both “Automatic outdoor mode” and “Enhance color” turned off.

>My average SOT was between 4.30h and 5h on a day and half between charges. Sure, it doesn’t sound much but keep in mind that 4G and WiFi were always on. Based on my experience on other ROM’s this is what I normally get.
And keep that in mind that SOT is only a mere evaluator on battery performance since, for example, when I was travelling I putted my phone on “Airplane Mode” and watch a 2.30h movie and taking some (CLICHE ALERT) cloud photographies, managing to drain only 35% battery achieving 3h SOT. Most people care too much about SOT where it can be very different from user to user based on their normal usage.

> With this in mind and judging on my daily usage, FlexOS battery performance is marginally above average with other CM based ROM’s that I have been trying lately. Remember that you can achieve better performance (or worse for that matter) if you use your device differently or if you use a different kernel and tweak it to suit your usage.

### Customization
One of the big reasons users choose to ditch the stock firmware and move to a firmware like ours is that we offer added functionality as well has customisation options. On the FlexOS, customisation was one of the top priorities and everything could be found in the FlexControl section in the Settings app!


The reviews say :

> Flashing a custom ROM we always look for that “custom” part, where and what we can change to make it look unique and to make it truly ours. In FlexOS we have the obvious but straight to the point “FlexControl”.
> What I think about the FlexOS is that, for me, it hits the perfect spot in the customizations department: not so many but not so little. On my personal taste it gives me just the right amount of control. I ran Resurrection Remix and Blisspop a few weeks back and the amount of customizations on them were endless, I spent so much time on customizing that I experience many UI crashes specially on Blisspop (you can check our Blisspop review) that I needed to cut down some features to have a stable experience. Moreover, being a CM based ROM you have access to the CM theme engine which gives you a lot of flexibility customizing different aspects of the UI. But it all comes down to your personal taste on how customisable you want a ROM to be. But rest assure that FlexOS gives you plenty of control on no expense of smoothness or stability.

As mentioned earlier, FlexOS gained a lot of popularity, and that can be estimated by a simple [google search](https://www.google.com/search?q=flex+os+rom&oq=flex+os+rom). Some of the reviews can be found here :

<iframe width="560" height="315" src="https://www.youtube.com/embed/fy4g2oUGSBQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/XbrjthiMHYc" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/Oz-nG0v3Mqk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/T_tPVu6uPs0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

