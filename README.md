Whatapalaver's 100DaysOfCode Log - Round 4
===

I've been in my first developer role for about a month and it's clear to me that I am going to have to take my journey to "hot shot professional coder" as seriously as I took the bootcamp experience. I can't afford to drift through the experience and instead need a defined developer's development plan to work through. Something like this [fine roadmap](https://github.com/kamranahmedse/developer-roadmap).

So, with that in mind it's time to kick start Round 4 of 100daysofcode to document the progress and keep me accountable.
My previous accountability rounds are till available here:

- [Round 3](https://github.com/Whatapalaver/100_Days_of_Code/blob/master/r3-log.md) documented the 70 days post Makers graduation where I consolidated the bootcamp experience, completed a stack of technical tests and finally secured myself a couple of job offers before accepting a fullstack role at The V&A.
- [Round 2](https://github.com/Whatapalaver/100_Days_of_Code/blob/master/r2-log.md) covered the 99 days of my Makers bootcamp experience. From the pre-course to graduation day.
- [Round 1](https://github.com/Whatapalaver/100_Days_of_Code/blob/master/r2-log.md) This was my initial foray into 100 Days of Code.

R4D13
---

Everytime I try and setup a Python dev environment I end up in a whole heap of poop! It was going relatively well today, I sorted the $PATH bit that normally confuses me and even set up Virtualenv but I rand into headache zone when I tried to clone a repo into a virtualenv and then lurched from one head bang to the next. By the end of the day I had finally set up my environment with a Vagrant box and an Elasticsearch instance so I could quickly race through some exercises from the excellent Relevant Search book by Doug Turnball and John Berryman. At least I'm in a good place to crack on tomorrow.

R4D12
---

Found a great toold for testing custom ES analysers and then discovered its now broken for the latest version of ES. That took quite a few hours of hairpulling and Stack Overflowing but I had the bug confirmed. I then discovered the more manual but still useful \_analyse with explain: true which just about saved the day.
Started a FEM course on JS - From Fundamentals to Functional JS with Bianca Gandalfo. Pretty good so far.

R4D11
---

Creating custom analysers for elasticsearch. 
Also explored html5 canvas which is cool.

R4D10 Mon 4th Mar
---

Much Reactivesearch hair pulling today. Experimented with copy_to to create new keyword in my index. Failed to get the nested - multiobject field to render in the multilist component. Had a minor success when I managed to display categories only to discover the results were rubbish. Ended with a high though - finally managed to get ternaries to work in my react component so that non existent images didn't crash my app. Yay!
Also dabbled with JS30 and JS transitions with flexbox.

R4D9
---

It's proving to be a pretty good move to have reverted to JS fundamentals. So far I've learned some useful stuff but also revealed some simple misunderstandings with things like variables and references to objects. I ended up getting myself 2 downvotes (and counting) on stackoverflow for my naivety but at least I got a number of useful answers that helped me slap my forehead in realisation.

R4D8 Sat 2nd Mar
---

Still on Vanilla JS experiments thanks to Wes Bos. Completed no4 the css variable exercise. Pretty useful stuff.

R4D7
---

Trying to fathom out why Reactivesearch is doing odd stuff to my empty fields was a great opportunity for exploring chrome console. There is just so much stuff to be revealed by that tool. I've typically ignored the network tab but this one enabled me to see the POST header and the body returned. That enabled me to fathom out how the library was converting its default query into a true elastocsearch query. Still, haven't exactly solved my problem but I'm on the right track and have my sleuthing tools lined up now.

Also a css and js clock from JS30.

R4D6
---

I was juggling between vanilla JS with CSS and Elasticsearch today. I started the Wes Bos 30 day challenge last night as I'm aware that I have leapt over the basic 'manipulating the DOM with vanilla JS' stage of my learning. Today I was therefore making a little drumkit for the browser, moderately jazzed up with css grid.
I also worked on Reactivesearch experimenting with the very beta implementation of support for nested fields. I had some significant excitement as I fathomed out now end of bugs and glitches and really felt a lightbulb moment as the momentous power of chrome inspector was revealed to me.

I wrote an abstract for a potential lightening talk at a German IIIF conference later in the year. Here's hoping its not accepted.

R4D5
---

So it's back to ElasticSearch today, this time trying to bring in the V&A objects data into my experiment with the Reactivesearch frontend. I've ended the day with some cool visuals of the ceramics collection using the resultcard component, I do however have a gazillion new issues to resolve! Our ES data is riddled with nested fields and the release of ReactiveSearch that I had been using doesn't support it. I've since upgraded to the version 3 beta which appears to have some form of support implemented although not seemingly documented. That will be the fun task for tomorrow.

In addition of learned 

- some css tricks about increasing specificity to override some weird styling imported in one of my npm packages.
- managed to debug a volume mount between my local machine and Docker which should mean I can work on this on my home machine

R4D4
---

Ben (from Makers) very kindly offered to review my manifest-pdf script over the weekend and he gave me some excellent pointers. Today I had the opportunity to work through some improvements which involved a bit of class extraction, improving the structure of my CLI, adding a config file option so you don't have to pass a gazillion flags in the run command and a general tidying up of my initialise method. I just need to retrofit some much needed tests!

R4D3 Monday 25th
---

Struggling with Elasticsearch again today, dabbling with some frontend integrations but finally having some success with Reactsearch which provides React components to work with an elasticsearch instance. I was able to mock up a dummy interface with some high level facets and added some uber cool illustrations courtesy of robohash.org . I need to explore nested fields next.

R4D2
---

I wanted to practice with some end to end elasticsearch work. I've been working on aggregations and nested queries but all within kibana. I feel the need to work it through with a full application to try and seal some gaping holes in my conceptualisation. I thought it would be great to kill two birds with one stone and work this through in python....
Hours lost.
To fathoming out virtualenv and then virtualenvwrapper and then trying to fix $PATH errors and blah blah.
Bottom line is that I got no further than an extremely rudimentary Hello World in flask. No where near elasticsearch at all.


R4D1 - The development plan unveiled
---

In my first month at the museum I've worked across a variety of projects. Working on tickets that fix features on the CMS (a Ruby on Rails application), created a mini executable that translates a IIIF manifest into a customisable pdf document, becoming a leading expert on regex (cough), panicked myself with ssh commands and explored elasticsearch in depth.

There is just so much that I don't know and what I do know, I know I don't really know. There is plenty of opportunity for performance anxiety.

Here's my initial attampt at a pathway to Fullstack competence with a heavy nod to the fact that I'm in a museum - hence the IIIF and Elasticsearch focus.

![Operation Fullstack](r4d1plan.jpg)
