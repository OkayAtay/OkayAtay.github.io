---
layout: post
title:      "Lessons Learned from 1/2 way through JQuery Project"
date:       2018-08-30 23:14:56 +0000
permalink:  lessons_learned_from_1_2_way_through_jquery_project
---


My 100% intention was to buzz through the Jquery project. All it really entailed is updating some straightforward views from Rails to Jquery. Well, my hubris has brought me down a few pegs. JQuery is no joke. So, to prevent any member of the reading audience from repeating my mistakes (*cough* getting stuck for 3 hours pleading with the asset pipeline to kick in as easily as it had done during the labs*cough*) Here are some tips from the mid-point. 

Lesson 1: **The Asset Pipeline is not Magic**
Yes, this is true this canny trick of loading and compiling js files does not just happen by one closing one's eyes and believing. There are some very necessary steps that took me quite a bit to figure out. 
1. include your file in your `application.js` , it will look like this: `//=require <filename>`
2. head to your `assets.rb`, which is located in `config > initializers` and add it to this file, that I believe compiles your JS files. It may be that you just need the line of code `Rails.application.config.assets.precompile += %w( applicatoin.js )`, but b/c I'm trying to be thorough I added one for every js file that I have to deal with. 
3. make sure your `<%=javascript_include_tag '<file>'` is somewhere in your html. I plopped it into my `application.html.erb` and it seems *fingers crossed* to be consistently functioning. So I'll claim that that's the right way to do it.

Lesson 2: **PLAY IN THE CONSOLE**
Why in the world did I try to figure out the perfect code in my file **before** using that beautiful location in your browser where you can experiment with your views real time? I don't know, but that's now the old me. Bye 'non-console-utilizing' Felicia. 

And Finally -- 

Lesson 3: **When in Doubt, use Vanilla JS**
Turns out the world is shifting, vanilla JS can do a lot of what jquery can do AND what's better is that it doesn't output ugly convoluted objects where you have to tab down a million times just to find some basic text. Obviously, the project calls for jQuery, but don't kill yourself trying to drench your code in $$$$$$$$. 

Hope this helps, I'm only 1/2 way through this lab, so really-- I can't claim to know much. But, a little goes a long way.
