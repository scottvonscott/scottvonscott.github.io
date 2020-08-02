---
layout: post
title:      "Something, something, "Off The Rails""
date:       2020-08-02 21:39:15 +0000
permalink:  something_something_off_the_rails
---


I’m personally lucky that my wife and I like to stay organized with so many aspects of our lives. My Rails project was yet another idea (after Sinatra) that I was able to directly lift from an active spreadsheet that we maintain together, travel planning.

For anyone who strives to make the most out of their travelling and vacations, you know how much work can go into researching and the logistics of planning a trip. You’re probably spending a good chunk of savings and time off work, and it very easily may become a prominent memory for the rest of your life. Travel planning usually entails maybe 10-15 open tabs, pursuing reviews, descriptions, maps and more, taking all of it in and hoping what you come out with will meet your expectations and be worth all the time and effort. Wanderlust was the app I made to browse and track the places you want to go and the things you want to see when travelling the world.

The wonders of Rails generators really are impressive to behold when you first get started, it looks as if a day of work is done in maybe 5 minutes. The sheer amount of automation and tools available in Rails can make anyone feel like they’ve been building apps for years, but it can become very obvious, very quickly that the advanced sophistication of this framework unsurprisingly demands a more sophisticated comprehension of what’s under the hood.

The most prominent example of my hubris was a double nested form that provided for object selection or submission when planning one of your trip days. My controller setup did not care for this “either/or” input my form was sending and what was essentially the primary load-bearing element of my app was dead in its tracks.

Desperately I wrote what would turn out to be the most nightmarish block of code yet, 15 lines of specific strong params conditions, including a 10 line private method that scrubbed my incoming params of “unnecessary” data. Before even finishing, I knew it stunk of everything we’re taught to avoid. Of course this problem had likely occurred to someone, and of course there was likely a simple tool in Rails to address it. Sure enough, inserting :reject_if beside my accepts_nested_attributes line in my models was everything I needed.

This problem highlights two primary lessons to me. First, that useful gems and frameworks like Rails are easy to take for granted, and how important it is to maintain an understanding of them inside and out. Secondly, that as dry and sterile as reading documentation can be, it’ll likely save your butt when your app stops in its tracks. Bottom line, Rails is a great partner when developing, but you still have to pull your weight.

