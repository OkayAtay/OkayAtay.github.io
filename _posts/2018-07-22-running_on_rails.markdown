---
layout: post
title:      "Running on Rails"
date:       2018-07-22 18:45:49 +0000
permalink:  running_on_rails
---


I am currently working on my Rails Project, and realizing connect, creating, and implementing models through Rails is no joke. Yes, it is less manual than Sinatra -- but with all the data bases to keep track of I do find that my head is spinning trying to ensure that I am DRY(ing) and Restful(ing)  and MVC(ing). 

I far from have all the answers, so I think I'll write about a concept where I'm currently struggling -- document the good with the bad, right?

In my project, I am creating a 'Traveler Tracker', which allows users to create iteneraries. My 3 Models are Travelers, Trips, and Attractions. 

A Traveler  - `has many :trips` and `has many :attractions, through: :trips`
An Attraction - `has_many :trips` and `has_many :travelers, through: :trips`
And Finally ..
A Trip - `belongs_to :traveler` and `belongs_to :attraction` (and is also acting as my join table)

So this is where my woe begins. I want my Traveler to be able to create a `Trip` and add `Attractions` to their trip. So the division is no longer as clean as my models have led me to believe. 

I have tried `accepts_nested_attributes` for attractions to trips.

My models to do not like that and currently my trips are being created sans Attractions. A TRIP WITH NO ATTRACTIONS!?! That's pretty much chaos. Or called going nowhere.

As I'm typing, I'm thinking of what it's like to learn a new language. I recently visited Medellin & Cartagena Colombia and was forced to do some serious flexing of my conversational Spanish muscles. However, the magic of language, is that if you don't know the perfect word/way to say something than just try a different way (even if it's a bit round - about)

So, in typing through my frustration, I have an idea. Rather than create wacky connections that have me banging my head against the wall -- I'll just embed my "Attractions New" into the "Trip New" form. Hmm, maybe it will reload the same form and then the user can add the attraction that way? Unclear, I'll keep you posted. But hey, options.

Note: I still will need a way to have a #attractions method on my trip, but maybe I'll just do it manually? Messy? Probably, effective at problem solving and figuring out a new way to do things, yahhhhs.

Also, quick rant about 'helper' methods. They're not helping me >_<.  

*Welp, let's see how this goes. *
