---
title: 'Ludum Dare 41 Post Mortem '
date: 2018-04-10T00:59:49-04:00
draft: false
---

[ludum-dare-41](https://ldjam.com/events/ludum-dare/41/ludum-dare-41-4)
 
On this past weekend I participated in the Ludum Dare 41; The theme was "Combine 2 incompatible genres" I decided to take a shot at combining JRPG mechanics with slot machine mechanics. My mission was to do a deep dive into Godot engine and see if it's the "Unity killer" it's been shaped up to be.

#### Mission Accomplished!

![poker chip character](https://i.imgur.com/gONSE10.gif)

Although I'm not exactly worried that Unity will be dethroned anytime soon, Godot has certainly left behind a good taste. It's unique node system allows me to break everything faster than ever before, and that is definitely a good thing. With Godot I found it extremely easy and rewarding to just rip things out of my game to see what would happen which I can see becoming very powerful/scalable in bigger projects. Another thing that I liked a lot about the engine was its animation tools, very cool!


Alright, enough talking about the engine; lets talk about the game

### The Good:

One lesson learned from doing this game jam was that spending more time on a single section of the project is a double edged sword. I spent a very significant portion of my time working on the slot machine aspect of the game and it shows... in the other parts of the game. For all the time I spent making sure I could calculate every possible slot machine pattern, I lost time where I could have showcased other things. The coolest part about the over engineered slot machine is that it could calculate any pattern with any number of columns.

![screenshot of code](https://i.imgur.com/4nTDvcj.png)

Shown above is the code that calculates the slot machine patterns, I was trying to get around writing a whole bunch of hard to follow loops that I kept seeing in slot machine examples that I found online, of which there is few. It returns a Slotline type that holds all the values that you would need to determine the 'score' of the roll.

### The Bad:

Having slot machine mechanics made it difficult to not take choice away from the player. One way I could have tackled this is with some meta systems in place that would let the player apply buffs that would do some RNG manipulation or something. One mechanic that I ditched to save time was before you roll the slot machine you would choose what line was going to be your attack value and what would be your defense value.

![slots mechanic](https://i.imgur.com/TfkWbBS.png)

Above is the scrapped mechanic 
Red is the line for attack and purple is defense

### The Ugly:

Player feedback is one of the most important aspects of game design and it is completely absent from my game. The main player feedback system that is missing, is feed back from the slot machine. This is missing due to time constraints, but I digress. The player needs to understand what their roll means and how it is affecting them. The other side of feedback systems that is missing is 'game feel' I understood, before this project, the importance of game feel but now, it is very clear to me that good game feel is a necessity and not a 'nice to have'. For future projects player feedback will always be something that I will consider at every turn. The concepts that I think are important for game feel are outlined very nicely in this talk 'Juice It or Lose It', by Martin Jonasson & Petri Purho.

### Conclusion:

I have participated in a couple of game jams in the past but one thing that really made this one stand out to me was that my goal was not to just make anything, but to try and make something that is complete. I didn't really hit the target this time, but going forward this will always be my primary goal. A more specific goal that I will set for my next game jam is to put into practice the things that I have learned about time and project management.
