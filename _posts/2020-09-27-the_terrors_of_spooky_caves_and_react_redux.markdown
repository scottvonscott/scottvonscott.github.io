---
layout: post
title:      "The terrors of spooky caves and React/Redux."
date:       2020-09-28 03:30:12 +0000
permalink:  the_terrors_of_spooky_caves_and_react_redux
---


For my final project, I wanted to have some fun. I had created a trivia game for my CLI project (our very first project) and I wanted to wrap things up in a similar way, especially considering most of the others made with Ruby and JS were meant to emulate popular websites. No, I wanted to do something a little different.

What I came up with is "Bork!" a dungeon diving, monster slaying game that allows you to brave a spooky cave to save your puppy.

The game mechanics are super simple, and if you've played rock-paper-scissors before, then you already know how to play! The difference is that you and monsters you face both have health that will dwindle with each round lost. Can you survive long enough to get to the bottom?

Speaking for myself, this project was a bit of a challenge because Redux still feels like a really expensive gift that you didn't know you wanted ( and still aren't sure you do). Accessing and manipulating state with React alone was just getting comfortable when Redux rolled up and changed the game (har har).

That being said, I do admire and appreciate its adherence to the "single source of truth" principle that we all now have tattoed in our brains. My app wasn't massive by any means, but the more I ponder ways to expand and improve it, the more I found myself relying on the assumption that each and every component can reach out to Redux if need be. It's the perfect example of another tool in our toolbox that we've developed personal judgement about using or abstaining from. That kind of judgement is what makes us versatile future developers.
