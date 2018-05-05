---
layout: post
title:      "Sinatra Portfolio Project Thoughts"
date:       2018-05-05 13:57:59 +0000
permalink:  sinatra_portfolio_project_thoughts
---



About 80% through my Sinatra portofolio project, I'm realizing that simplicity is key as I build the web pages and overall coding skillset. 

I have a new role that development-adjacent and to create code that others can identify it's purpose easily is prime to the success and continuity of any project. Going forward, my goal is to hone my ability to create crisp, clean code. Similar to writing concisely, less is often more difficult to generate than more -- but I think it's a worthwhile goal. 

In Sinatra World --  here's some lessons I've learn from 80% of this project: 

*Database & ActiveRecord*
How you set up the database really sets the tone for what your classes will do in the future. Take the time to think through what properties you want each class to have. And use password_digest rather than 'password' to ensure that your has_secure_password will function!

*Controllers*
Separating out the controllers is essential for identifying roles and responsibilities. It can be so overwhelming to look at all the web pages at the same time. To prevent confusion, make sure you understand the user journey so that you can easily map/understand the order of events

*Models*
Crazy how in prior labs we spent so much time in these models, defining behaviors and now they simply help us define our relationships between models. Our 'has_many' and 'belongs_to' associations ensure that we can can display the right data 

*Views*
Last, but not least, views -- honestly my favorite part. The views are the front end, what users see -- and the bits that bring all your hard work together. They too should be kept separate like in the Controller. The 'create', 'edit', 'index', 'show' and other functions make it clear what the user can do on each page

In Summary -- keep it simple, separate and have a good time!

Wish me luck, I'm almost done!


