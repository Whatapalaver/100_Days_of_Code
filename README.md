# I've joined the #100DaysOfCode Challenge.

If you've decided to join:
Check out [the Official Site](http://100daysofcode.com/) for the #100DaysOfCode movement. Connect with others on the platform of your choice from this list: www.100DaysOfCode.com/connect 

### Whatapalaver's 100DaysofCode
I started my first round of #100DaysofCode when I decided that I was going to be starting the Makers Academy bootcamp. I didn't exactly code everyday and I didn't maintain the log on all the days I coded. Nevertheless, it proved to be a good motivator for action and it is still interesting to see the progress and frustration levels over that time.
You can see that log here: [Round 1 Log](./r1-log.md)

# 100DaysOfCode Log - Round 2 - [Angela Wolff]

This is the log of my second #100DaysOfCode challenge. 
I've decided to set-up round 2 to coincide with the start of Makers Academy pre-course 11th June 2018. 

## Log

### R2D26
Start of Week 2 of the Makers course.
Had a code review in the morning and went through my solution for the airport challenge. Had some good suggestions for improving RSpec test readability.
Started the [Oystercard challenge](https://github.com/Whatapalaver/oyster_card) 
Updated my [RSpec gist](https://gist.github.com/Whatapalaver/8fee69a56a2c519f45bdcdaf07b886c6)

### R2D25
I've now spent hours on the airport challenge, and still not finished - phew!
I now understand stubbing for things like removing randomeness from methods so you can test specific cases.
Used a lot of describe classifications and contexts to neaten up the RSpec tests and make the read out more informative.
I need to update my github gists with some RSpec examples.

### R2D24
Start of the weekend challenge today - [The Airport Challenge](https://github.com/Whatapalaver/airport_challenge)
First learning was how to set up a feature test in RSpec (as well as the unit test) so that I don't have to deal with all that irritating repetition in irb.

### R2D23
Again I had a morning of RSpec and TDD. The whole process really impresses me it's like the David Allen "GTD" approach to code. By iterating through failing tests that you intentially create you steer yourself through complex projects step by step, only ever revealing the next obvious step. It's a great way to avoid overwhelm.

Had a nice challenge of testing between `return`s a value and `puts` a value for our test calculator app.

Also flipped over to using VSCode as my test editor although I'm super uncomfortable about sullying my macbook with microsoft apps.

More pairing in the afternoon. I was with a focussed go-getter today so we stormed ahead, ticking off tasks in no time. Really productive for me and I learned some cool methods for grouping and describing RSpec tests around th method or class being tested. That gave me the structure and organisation that I felt had been missing from my test scripts. 

### R2D22

Started the day worried about my rspec abilities after leaving last night with a messy spec file and a failing test. After literally hours I discovered that the failure was down to a simple cock-Up in the way I described the path to a required file. Everything else was fine. 

Still, by then I had identified a perceived rspec ineptitude and had bought a new book “Effective Testing with RSpec3”. Yawn. I jumped between the book and a practice dice app that we were using to practice test writing. 

I managed to write a test that approximated a test for randomness. Was the dice roll actually random or convincingly not non-random?

Pair programming in the afternoon which ended up being mainly chat. Very interesting chat with a little bit of code. It helped me to try and run through some conceptual struggles with my pair and challenged my understanding. 

### R2D21
Day 3 of the onsite Makers course. We started getting to grips with TDD and after my work through of the Boris Bike challenge it finally clicked for me the linkage between feature tests (derived direct from user story) to unit tests written in rspec. i spent the morning drawing a TDD decision tree. 

The afternoon was back to pairing on BB with a new colleague. we had to go back a few stages so I wasnt driving. I find it very hard to maintain focus for a whole afternoon when not in control. 

I learnt that rspec is way more intelligent than I had given in credit for. It has me licked and I now need to spend time getting to grips with it. 

### R2D20
Started the morning recapping hashes and discovered why some of my attempts weren't working yesterday. In some cases I had the syntax setup correctly but I was having a problem with the return - sometime you have to specificy it directly. Its a good lesson to make sure you understand why something fails rather than just rejecting it and randomly testing out other random shit.

In the morning I started the airport challenge on my own and started to panic as there were no step by step instructions and it felt like my stabelisers had been whipped off my bike.

The afternoon was back to pair programming and the Boris Bike challenge. This involved much more hand holding which will help when I go back to the airport. We worked through feature testing in irb and rspec set-up. In rspec I learned the new test:
 `it { is_expected.to respond_to :working?}`

### R2D19
First day onsite with Makers today. Loads of set up and introductions but in the afternoon we started on the pairing process. Each day we will shift to a new colleague to pair with. Today it went well. We attempted the driver navigator technique as we puzzled through hash transformations. I realised I need to get a grip with enumerable so that I can explain exactly what .inject does rather than just copying it verbatim. Learnings today were setting up our first github repo with collaboration. Initially we went for the approached of each using the same remote. I'm sure we will move to forked repos, branches and ultimate merging, but slowly, slowly. If I don't drink too much wine this evening I will also suss out enumerable.....

### R2D18
Last day before the onsite main course starts at Makers tomorrow!
I finished the roman_decoder, refactoring to use my nemesis - hashes....

### R2D17
Having met my Maker's mentor last night, I have been invigorated to try using TDD to control my solution to the roman numeral decoder challenge I'm working through. It actually proved to be a pretty effective way to work towards a solution. I went with the approach of:
* write a failing test
* hard code the result to fix the test
* write another failing test
* implement simplest bit of logic to fix test
* repeat

The output was long-winded but it worked.

### R2D16
I’ve returned to Chris Pine’s Learn to Program book and am working through Chapter 9. i enjoyed the Roman Numeral challenge and am now puzzling over a spin off - Roman Numeral Decoder. I’m finding it delightfully challenging. I know what I want it to do but I’m not sure how to do it. I suspect it will be a mix of slice! match and regex. Ughhh I hate regex. 

### R2D15
I had a go at a React javascript tutorial today at [ReactJS](https://reactjs.org/tutorial/tutorial.html)
I have a sense that I might have wasted my time. I barely understood what I was doing and just followed instructions blindly. I have learned that JS is riddled with brackets and semi-colons and de-bugging is going to be one heck of an arse! 
I spent the afternoon pairing with another pre-course student. We rotated the navigation/driver roles and I found it to be pretty useful.

### R2D14
I cemented quite a lot of knowledge with the student_directory challenge today. Saved and loaded data from csv files. Grasped the concept of ARGV (runtime arguments) and the then necessary specification of STDIN (standard input ie. keyboard) for .gets as otherwise it would default to the ARGV input. I also just about grasped the use of instance variables dfue to scope. While I've used these before I didn't realise we could bypass it by setting the variable (defined elsewhere) as an argument to a method.

All good stuff. Plus. I combined the pomodoro method with sourdough production today as the timing was perfect for the dough folding stage.

### R2D13
I started the student-directory challenge today. It was pretty challenging. Designed to be a simple example of how to take a github project from strt to finish - it left me struggling with hashes or at least arrays of hashes yet again. I'm beginning to see a theme of hash mental blocks. I reviewed previous students commits and found a really good (understandable) solution by Simone. I reckon there is a fine line between cheating and admirable researching?

### R2D12
I'm supposed to pair programming but haven't managed to arrange this yet. So instead I ran through the FizzBuzz exercise and set up the Rspec testing code on my own. I can only do equality checks at the moment and imagine rspec can get a lot mopre complex. 

I also did some more codewars kata, these are getting remarkably easier to cope with which is a huge leap from those early days of having zero clues!

### R2D11
I'm away visiting my parents this weekend so haven't had much opportunity to code. I did work on some bug spotting for other students which is helpful for me and read more chapters of the Chris Pine book. In the sun. With beer....

### R2D10
I'm still on the Ruby Koans. I'm sitting in Costa tethered to my phone's network while systmatically sticking in the right answer to satisfy the ruby deity. I'm not convinced if I'm learning enough on this course. The error messages give you the answer and while that might be part of the learning experience, I get it now, and have 200 more boxes to tick. There are some other bits and pieces being added to my knowledge base though so I will persevere for longer.

### R2D9
I finished the mastery curriculum today with the start of a simple todo program which demonstrated working with classes. Now its time to work on some extra Ruby tutorials. As we've spent quite a bit of time trying to fathom rspec error messages I've decided to give the [[Ruby Koans](http://rubykoans.com/) - route to enlightenment a go. It's proving interesting...

Also tried to help another student out with some troublesome code that she had been struggling with for hours. It reminded me how wedded you can get to code you have struggled over even if it is fundamentally flawed. Sometimes it can be as well to start again from scratch and try a different approach. Learning the skill of telling someone that without right royally annoying them may take me a little while to master.

### R2D8
I started the day with a walk to the allotment while I watered the crops while pondering the hash challenge waiting for me at home. It's what is known as "procrasta-gardening". Anyway, I cam home feeling fairly nervous about the the last hash challenge in the mastery-curriculum, but it was smooth(-ish) sailing. Job done!
Onto methods now....
Quite an intense afternoon trying to refactor my Blackjack methods so that they passed the test. I wrote a working program pretty quickly but ignored the instruction to keep my methods to a single task. You should be able to name a method without the requirement for an "and". I'm afraid all mine were multi-talented for a while.

### R2D7
I have spent hours trying to solve the crocodile invested water problem today. Finally got a solution, splitting arrays and testing for presence of croc "C". I reckon it could be improved quite substantially but I'm feeling eager to move on. Hashes next.

During the afternoon I spent more hours puzzling over the array of hashes question. If I was brave I would post something on Stack Overflow but they are pretty brutal over there.

### R2D6
I've been struggling with a challenge from the mastery-curriculum. We need to push a user specified list of names, sequentially into a user specified number of groups. I found this quite tricky until I decided to create a nested array with n arrays within the outer wrapper. I was quite pleased to have solved this one.

### R2D5
Does playing with new themes for iTerm2 actually count as coding? If it helps I have really cool Terminal now! 
I did solve the ruby tweet redaction puzzle that I struggled with yesterday so that definitely counts.

### R2D4
If we don't count weekends (and who does?), we are already at the end of week 1. OMG. I am going to be a junior coder looking for a proper job before I can even blink.
Today I was working on loop programs with a simple text based game.
There was also a fair amount of problem solving going on as we had to do pull requests on the command line repository and it seemed to generate a load of errors across the group. Mine worked fortunately but trying to resolve some of the other problems was challenging to say the least.

### R2D3
This is actually day 4 of the pre-course. i was in work yesterday doing a handover and only managed a small amount of very basic SQL - hardly counts as coding.
Today I am back on the mastery-curriculum and have just finished writing a neat dice throwing match, using a while loop with conditionals. Onto FizzBuzz now if I can fathom out what that is...

Well FizzBuzz proved to be reasonably straightforward at least in comparison to the fibonacci sequence. Chapter 4 also included a new code style checker and that was fussy! Frustrating. 

### R2D2
Day 2 of Makers Academy and I finished the Week 1 workload by lunchtime. There are still loads of optional extras to work through on command line but I'm tempted to see how challenging the Ruby workload is while I have a chance of bagging some time.

The command line mystery challenge was fab and really surprised me with how nifty you can be with just the terminal. It has inspired me to try "Learn UNIX The Hard Way" later. I will feel like a real hacker then.

The afternoon was spent familiarising myself with the Ruby Mastery Curriculum.

Also flipped this previously forked repositry to a stand alone so I get the benefit of my commits.

### R2D1
I'm still waiting for the pre-course details to be delivered to my inbox, so in eager anticipation, I turn back to Codewars and dabble until I rank upto 5kyu. I am slipping back to SQL kata as I find these so much easier than Ruby. I won't let Ruby slip too far, in fact it will get all my focus over the next few weeks but I do enjoy testing my SQL skills from work.

The pre-course email is in and I am now wading through introductory courses on command line and the terminal. I've never found this terribly exciting which will be why I still struggle to navigate my way around. Not for much longer though.

I finished the command line and github tutorials. I can highly recommend the Git-It desktop app for working through the git workflow. It's fantastic.
