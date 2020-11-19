---
layout: post
title:  "RapidDraw (2017) - A three-day experiment to recognise hand-drawn doodles using a mobile neural net"
author: aniruddh
categories: [ Apps, Machine Learning ]
image: https://aniruddh-chandratre-e877.netlify.app/static/9566701b941243f35510cd8abf7b470f/57198/22550499_2091868827505708_6858246366187950784_o.jpg
toc: true
---


## The fundamental question
Can artificial intelligence recognise human-made doodles?

Google had their own experiment called QuickDraw to verify this, and it was quite successful. But, it is hosted on a huge cluster of servers, and is constantly trained and improvised. But as we move into the future, we shift to the mobile generation. So the question is

> Can a neural network running on your mobile device recognise your doodles?

This application is built as an experiment to answer the same. The best part? It is [open source](https://github.com/C-Aniruddh/RapidDraw) for all the free minds to experiment on existing code to make the most out of it!

Every time you play, you'll be given 8 random objects to draw (from nearly 100 categories), and the app will try to guess it! It may not always work, but let's see how well it performs for you!

## Day 1: 15 October, 2017
The question if a neural network running on my mobile device can recognise hand-drawn doodles strikes my mind. But how can I test this? I know that QuickDraw exists and the data for that is open source. So I start from there.

Quickdraw provides thousands of categories for hand-made doodles in different formats. So I downloaded around 110 categories and I wrote a pre-processing script which converted all the images from the npy file to jpegs such that I can make use of the training scripts that have been made available by Google. The script can be found [here](https://github.com/C-Aniruddh/RapidDraw/tree/in-dev/processing), along with [instructions](https://github.com/C-Aniruddh/RapidDraw/blob/in-dev/processing/process_all.py). This said and done, How do I run this on a mobile device?

Luckily, for me, there is a lot of news and talk about how MobileNets can be for image classification at the edge. I get right into it and train a basic model for classifying images. But now I need an interface where someone can draw! So I fire up Android Studio and build an extremely simple app! Have a look!

<iframe width="560" height="315" src="https://www.youtube.com/embed/nOrEPy8cWyU" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

So now I start adding more and more categories and convert this idea into a game!

## Day 2: 16 October, 2017
Design, design, design. The entire day was spent into designing a layout and the flow for the rapid-draw game. 

## Day 3: 17 October 2017
After about 2 days of design and testing, I have a fully functional game! A few UI tweaks and its ready to launch! Have a look: 

<iframe width="560" height="315" src="https://www.youtube.com/embed/l3oKXSOqCZk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

