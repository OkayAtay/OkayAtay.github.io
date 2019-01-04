---
layout: post
title:      "React/Redux or Bust"
date:       2019-01-04 17:45:12 +0000
permalink:  react_redux_or_bust
---


This is my final (or close to final) post of my time at the FlatIron school. As a student working full-time it's definitely been a challenge to consistently work through the curriculum and devote the necessary time to the more time consuming final projects. I had grand aspirations of finishing the curriculum in a smooth 8 months, Sept - May, like an actual school year. That 8 months became 15, because the reality is that life is busy and summer in NYC is way too fun to be spent agonizing over small bugs in my code. 

My React-Redux Take-Aways

**What's a Store?**
Don't think 'supermarket' think 'storage'. The store is where your updated states (across all objects) are kept. You can update your store through your reducers/actions. 

**What's a Reducer?**
A reducer is where your updated values are passed from the action to the store. Ever noticed in the code that you pass something called `action.payload`. Your payload is the new data values that you want to utilize to update the store. It also dictates what you want to be return from the 'store'. 

**What's an Action?**
This is where the knitty-gritty happens. Need to make a fetch/post/delete request, you do that here in actions. Once the data is received then you can use it to inform how your components load/update or even delete. 

**What's a Dispatch??**
In the midst of all the redux lesson sometimes it can be hard to track down what is happening where -- And that is where a knowledge of DISPATCH comes in handy. Dispatch is what connects your actions. reducers, and components. Dispatch allows you to render the data from the store as props and conversely connect an action done on the client to a backend import. (e.g. I have a like button I can click, when I click this like button then the number of likes increases by 1)

In summary, redux is not easy, BUT if you consistenly arrive at each piece of the puzzle and think, 'what am I doing here?' you can navigate and maybe even potentially be comfortable with it. ALSO, 

IMPORTANT -- create your API FIRST, and then use seed data to ensure your displays are working. This will save you a ton of headache in the long run.

My Over-all FlatIron Take-Aways

**CODE IS IMPORTANT (& not scary)**
Though my career seems to be heading more in the direction of Product, understanding front-end and back end programming functionalities and how APIs work is essential. My understanding of coding languages helps me every day in my current product manager role. It helps me better speak to my engineering teams and is a great entry point as I expand my knowledge into languages like Swift, Java and Kotlin.  

**CODE IS IN THE DETAILS**
In my time learning I have become a much more detail oriented person. I love that some of the best coders embrace their laziness. The goal isn't to struggle! It's to be as resourceful as possible to solve problems quickly and effectively.

**CODE IS COOL**
My nerd street-cred after finishing this program is *way* up. While I still have a ways to go, I feel infinitely more comfortable speaking about topics in technology and no longer shy away from technical conversations. So, YAY for confidence!

So if you're just starting this journey -- know it's going to take longer than you expect, it will be moderately painful and oh man you'll be happy once you're done. But you'll learn so much along the way, so don't get discouraged, ask questions and embrace your inner engineer!
