Whatapalaver's 100DaysOfCode Log - Round 6
===

Round 6 of 100 Days of Code will document my 10 week (and beyond) Journey to become an Algorithmic Whizz. This year I intend to get to the end of Advent of Code without it sucking every waking hour.

- [Round 5](https://github.com/Whatapalaver/100_Days_of_Code/blob/master/r5-log.md) this was supposed to cover my foray into BDD practice but I abandoned logging after 3 days so we will never know how that progressed.
- [Round 4](https://github.com/Whatapalaver/100_Days_of_Code/blob/master/r4-log.md) this covered the first 9 months or so of my first fullstack developer role
- [Round 3](https://github.com/Whatapalaver/100_Days_of_Code/blob/master/r3-log.md) documented the 70 days post Makers graduation where I consolidated the bootcamp experience, completed a stack of technical tests and finally secured myself a couple of job offers before accepting a fullstack role at The V&A.
- [Round 2](https://github.com/Whatapalaver/100_Days_of_Code/blob/master/r2-log.md) covered the 99 days of my Makers bootcamp experience. From the pre-course to graduation day.
- [Round 1](https://github.com/Whatapalaver/100_Days_of_Code/blob/master/r2-log.md) This was my initial foray into 100 Days of Code.

R6D7
---

I'm still working through interviewcake (and still impressed). I've tried the brute force approach to determine the max potential profit from selling shares and then optimised using the Greedy algorithm method (so named because you choose the option that looks the best at every step). I find that spending time trying to analyse how I attempt the problem in my head is quite revealing as I rarely hold the brute force methodology in my head. 

R6D6
---

Had a significant hiatus but have rallied myself. I've been introduced to [interviewcake](https://www.interviewcake.com/article/ruby/data-structures-coding-interview?course=dsa) and while I haven't invested in the course yet but the free material is compelling. Excellent Big O explanations and the data structure explanations are the most compact and helpful that I've read so far.

R6D5
---

I’ve had a week+ off from daily algorithm and data structure training which is rearing its ugly head now that I’m trying to write a script to determine the height of a tree. I just about managed to implement a stack in python to create a brackets checker but now I think a tree recap is in order. 

R6D4
---

So today I watched videos on fibonacci and greatest common denominator. In with cases moving from a naive approach to an optimal solution. 

Some things that resonated:

- I always feel tres smart when I manage to get a recursive function to deliver the correct answer. I feel like I must be close to being recognised as a rocket scientist, so to see examples of where recursive methods to determine the nth Fibonacci number would taken longer than the time I have left on the planet was sobering. 
- another reason I’ve been scared off algorithms is that I am no maths whizz kid. I can’t remember how to work out prime factorials, I can’t even remember what they are. Given that Euclid is not my middle name how am I ever supposed to derive an optimal answer for the greatest common denominator problem. I suppose the answer is by practice and memorisation.

I do quite enjoy maths though, and watching entry level introductions to maths is not a bad way to spend an evening. I could either watch a khan academy video on the Euclidean algorithm or watch another episode of Grand Designs. Hardly any contest!

One realisation from today is that I am unlikely to ever encounter some of these data structures in real life. Ruby for example doesn’t have an implementation for a linked list and I will probably never need to write my own implementation as Ruby is not sufficiently “close to the metal”. If I had a use case where I needed to worry about memory allocation for performance reasons then I likely wouldn’t be writing in Ruby. 

R6D3
---

I've decided to quit auditing the [Data Structures and Algorithms](https://www.coursera.org/specializations/data-structures-algorithms) course and sign up proper so I can do the assignments. I've completed the first weeks challenges of 'Max Pairwise Sum' with optimisation. I suspect this will get hard pretty soon as there is a lot of focus on stress testing to deal with minimal feedback of failure.

I'm interlacing the basic algorithm course with the next level Data Structures course and covered off linked lists, which make a lot of sense but to my knowledge, I have never actually come across in practice. No doubt I will find out that I use them all the time but they are just not called linked lists in my language of the day.

I will finish the day with Doubly Linked Lists and may try and find time to read the relevant chapters in Grokking Algorithms so I can dream about data structures.


R6D2
---

Gayle Laakman McDowell (with HackerRank) presents some great videos which have been collated into a [CtCI playlist](https://www.youtube.com/playlist?list=PLX6IKgS15Ue02WDPRCmYKuZicQHit9kFt) and the [session on Big O](https://www.youtube.com/watch?v=v4cd1O4zkGw) was brilliantly described. I suspect I will need to do some basic math reminders on logs etc.

I need to draw up my route map asap. I can already feel myself spinning in circles as I wonder what to learn next. 

I was just looking at some optimisation methods for the first easy challenge on Leet Code and it involved discussion of Hash Maps. Wtf are hash maps I thought to myself as I committed to gaining at least a basic overview of Data Structures before I take on any more coding challenges.

Turns out I do know what a Hash Table is. It’s a hash (ruby) or a dictionary (python) and while I may not know how to implement one from scratch I do at least know how to use one. So perhaps I can continue after all….

So I paused on the procrastination and started watching videos. More Gayle Laakman McDowell (GLM) in my lunch break and [Data Structures](https://www.coursera.org/specializations/data-structures-algorithms) from the Coursera course I'm auditing after work. Already, with just 2 days part time study in my back pocket, I can see that this is a worthwhile exercise. Understanding how arrays are implemented as a contiguous area of memory helps me to understand the significance of things like in-place manipulation with methods! I can see as well, when I ponder whether my coding approach might result in an out of memory situation that it is possible to go from vague pondering to knowing. 


R6D1
---

I've spent some time reading around my challenge. If I want to achieve a decent level of algorithmic aptitude, I need a bit of a road map for the journey. So I've read the opening chapters of Cracking the Coding Interview (CtCI) and read other peoples blogs on how they achieved mastery on Leetcode.

I've signed up for a Coursera course on [Algorithms and Data Structures](https://www.coursera.org/specializations/data-structures-algorithms) as it was a regular feature in the blogs I read. I've watched the first weeks videos but I can't do the practical assignments as they don't seem to be available when you only audit the class. I'm not sure if I want to invest in a Coursera subscription at this stage.

Read a bit about Big O. Have to say that the explanation in CtCI lost me quite early on so I will need to recap tomorrow.

Did my first LeetCode challenge Two Sums but can now see that I've solved it in the most naive of methods with O(n2) despite thinking I'd snuck in a few optimisations.
