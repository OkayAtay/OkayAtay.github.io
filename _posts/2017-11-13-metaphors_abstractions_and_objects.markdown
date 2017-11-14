---
layout: post
title:      "Metaphors, Abstractions & Objects"
date:       2017-11-14 01:31:22 +0000
permalink:  metaphors_abstractions_and_objects
---


During the last 3 months of slowly and steadily making my way through the course material I’ve been regularly surprised by some of the knowledge I’ve gained. From the origins and intricacies of HTML, to the complexity of RegEx, and the interactions of OO Ruby – I’ve learned that web development is about how information interacts. It’s not magic, but it’s also not an exact science. It’s the spot where human creation meets high powered computer logic – a type of poetry where the two complement one another. 

Right now, I’m in the midst of OO Ruby labs, learning how a Class is a metaphor for a real-life object, and this abstraction can interact with other metaphors with behaviors created within methods. We started the section with Procedural Ruby, learning how to isolate a process into multiple steps. I even created a Tic Tac Toe game within the Command Line! But it makes sense that Procedural Ruby is just a means to learn how to think about the logic. Thinking through every step of a process as its own individual method is wrought with opportunities for human error. Also, it’s incredibly confusing for any programmer who needs to update the code afterwards. 

(Sidebar: That’s another thing I’ve noticed about coding – so much of it is about being “nice”/aware of those who will come after you. I love the inherent expectation of collaboration)

So I cannot lie, I don’t have OO Ruby mastered (yet), by any account. The “has many object” has just started to sit a little better in my brain. Of course, an Artist “has many” songs – and these songs are not just strings, they too are objects that hold their own unique information and methods. The schnazzy bit of code below shows the Artist example, and it makes sense. The code both assembles the songs in one place, but also theoretically makes the song aware that it belongs to the Artist and vice-versa.

1.	class Artist
2.	attr_accessor :name
3.	 
4.	def initialize(name)
5.	@name = name
6.	@songs = []
7.	end
8.	 
9.	def add_song(song)
10.	@songs << song
11.	song.artist = self
12.	end
13.	 
14.	def songs
15.	@songs
16.	end
17.	end

My next concept to tackle is ‘collaborating objects’. These metaphoric abstractions sure stay busy. 

