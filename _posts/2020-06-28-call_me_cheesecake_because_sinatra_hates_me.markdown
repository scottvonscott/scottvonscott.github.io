---
layout: post
title:      "Call me cheesecake because Sinatra hates me"
date:       2020-06-29 01:19:35 +0000
permalink:  call_me_cheesecake_because_sinatra_hates_me
---


It's a reference to a Guys and Dolls story, go look it up.

I'm being hyperbolic and self-deprecating per usual, I actually had a great time with my project. As with every project though, everything I thought I understood was challenged as soon as I ventured slightly out of the concepts that introduced me to the blue-eyed web application library.

I created a web app for tracking restaurant experiences. You might be thinking a yelp ripoff, and that's not exactly untrue, but the intention is more so to privately track and leave notes for yourself about the experience of dining out or ordering in. Given how 2020 has gone so far, it's been a lot more of the latter. Hot wings too hot? One sandwich big enough for two? Ramen egg hard boiled instead of soft? These would be pretty boring reviews, but as notes for the next time you order, they really help. I was already keeping a spreadsheet for this kind of thing, so it made sense to convert it with everything I've learned so far.

I was pretty confident in what I had built up until today, my routes were good, everything was interconnected and accessible. I had run dozens of tests with no problems, but eventually that came crashing down. I had updated an existing restaurant with a different city and it had saved no problem, cue me doing 20 other things before it all came screeching to a halt. All of a sudden my review form was broken, wouldn't even open.  Sinatra let me know it was hung up on the cuisine options (thank you Sinatra btw). What?!? So it all broke on the last day of project week, my updating the first class with the second class caused the third class to break because of the fourth class. Woof.

After some panicked investigating, I finally learned that my restaurant edit route was expecting attributes for name, city, and cuisine, yet the form was only getting name and city from the user. So when the edit went through it logged the cuisine as nil, which in turn was added to my list of cuisines. That one nil value smashed an iteration in my review form and gave me a headache to boot.

This project has been another humbling experience, a reminder to be dilligent and an example of how easily minor errors  can snowball into app crippling gridlock. It's still a little intimidating considering how complex real apps will be to build and fix, but cutting my teeth here will get me ready. One step at a time!

