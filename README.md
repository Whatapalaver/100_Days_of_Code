
Whatapalaver's 100DaysOfCode Log - Round 2 - [Angela Wolff]
=======

This is the log of my second #100DaysOfCode challenge. 
I've decided to set-up round 2 to coincide with the start of Makers Academy pre-course 11th June 2018.  
I started my first round of #100DaysofCode when I decided that I was going to be starting the Makers Academy bootcamp. I didn't exactly code everyday and I didn't maintain the log on all the days I coded. Nevertheless, it proved to be a good motivator for action and it is still interesting to see the progress and frustration levels over that time.
You can see that log here: [Round 1 Log](./r1-log.md)

Check out [the Official Site](http://100daysofcode.com/) for the #100DaysOfCode movement.

***Exciting News***
-------
I'm now combining my 100DaysofCode journing with Instagram, see [Whatapalaver Codes](https://www.instagram.com/whatapalaver_codes/) for additional visual excitement of a coding nature!

## Log

### R2D80
I'm just starting Conway's Game of Life today. I'm already fascinated by this challenge, not just because its a cool automated life animation but also because of it's potential for endless refactoring and logic refining. This will be a challenge on a par with the ten pin bowling scorer and I am going to enjoy it. While it's the logic coding that most interests me, I will use this challenge as an opportunity to practise some front end technology and may show the animations in React.

### R2D78
We finished our group project work today. It sort of fizzled out and while it was great learning experience, I'm not terribly impressed with what we achieved. In terms of features we didn't go much beyond the Instagram clones we individually coded over a single weekend. Admittedly we were totally new to Rails at the start but I think we lost the impetus of the regular sprints and we didn't entwine frontend and backend from the start. This meant that backend coders ground to a halt with more than a day to go for fear of creating something that would break the design. The design team were pushing with 2 mins to spare!!

In future we will plan the layout from day 1. We are hoping that with wireframes mocked up, designers, testers and coders will be singing of the same hymn sheet. Sprints will be scheduled in advance, with attendance strongly encouraged so that we can force some adrenaline into the process.

### R2D77
Absences and late starts across much of the team today so there was no opportunity for a rallying cry to action. I implented CRUD to the posts model and then filled out an application form for a cool health startup that have a load of interesting tech roles advertised at the moment.

### R2D76
Having solved the AWS hosting problems yesterday I felt the need to document the solution in a blog. As I had carelessly forgotten to take screenshots of all the error logs I needed to recreate the problem again. I couldn't quite bring myself to break the teams production environment again so set forth to retrace my steps in the Instagram weekend challenge. This time though I managed to set up AWS and the Heroku hosting almost with ease. Who thought *not* being able to create error could be almost as frustrating as not being able to fix one.
Here's the final blog post that details the [AWS debugging process](https://medium.com/team-rof/setting-up-a-rails-app-to-run-production-in-heroku-saving-images-uploaded-via-carrierwave-into-aws-c1cc28b0d6a6).

### R2D75
The AWS frustrations continued all day. Sam helped me suss out the heroku logs which slowly, slowly helped me reveal the problem which turned out to be a change to the hostname format following a redirection. There was momentous joy when an image finally appeared. 

### R2D74 Monday week 9
I spent much of last night and the early hours of this morning creating a branch on our facebook clone where I’ve stripped out all our DIY attempts at user authentication and replaced with Devise. Happily the team were keen to move forward with it this morning. 

We’ve just heard that a JS React frontend is desired for the project but we are being a little slow to respond to that as we have so many features to implement such as images, likes and comments. 

I got the images working using Carrierwave the gem that I used in my Instagram clone but it broke Heroku, which apparently doesn’t store images. 

That cued an evening of deep AWS frustration. 

### R2D73
Well who would have thought that Devise would make me sooo happy. What a joy of a gem that is. It does truly do everything and when it doesn't quite do everything (like add a username), its a doddle to amend. I can't believe I insisted we work without it on our facebook group project. I am going to kick myself everyday of next week as we struggle to test out authentication system.

Loads of progress made with the twitter clone today. I have a newsfeed with actual uploaded pictures and they are all assoicated with a user - yes of course the username is displayed as well!

Its a shame the styling is a total dogs dinner!

### R2D72 Weekend Challenge to rival Instagram
This is another rails challenge. I'm a few hours in and have just realised that rails ships with SQLite by default and all my experience is with PG. Not that inexperience is anything unusual.... but I am now wondering if I should start afresh, fathom out how to transfer across to PG or just suck it up and fathom out how to nail SQLite. It's something I need to add to my non-existent whiteboard of tips:
- Think about your tech stack before you start the project

Another thing I've learned is that it is really worth visiting the official site for any gem you plan to install and read the README. Who knew? They are actually pretty useful. My previous approach has been to riddle my gemfile with cool sounding gems, running bundle install and then wondering what they are and how they work. In an awful lot of cases they just do not work unless you perform some other arcane spell, only revealed in the README.

### R2D71
The team were back to a full establishment today so we started with a quick planning session and then cracked on with feature tests. We've run into a gnarly problem where test for authenticated users seems to prevent capybara from visiting the home page.

### R2D70
We had team absences today so I found myself working alone on the final stages of the signup and got myself snarled up in the intricacies of password_digest and has_secure_password. One of the coaches suggested we should have gone down the 'devize' route i.e. the plugin route of least resistance as that would have freed us up to be working on cool features like messaging and groups etc. Doh! I guess I'll be working with Devize this weekend.
The afternoon was not terribly productive either as I wasted time unsuccessfully implementing feature tests. Boring.

### R2D69
Day 2 already and the main challenge is to sort out user authentication (signup/login). Rails seems to have an app for everything but I pushed for us to avoid the easy route in favour of designing our own user authentication directly on rails (with bcrypt). My argument was that rails was entirely new and if we just go made installing one plugin after an other until we have a working app, we risked knowing no more at the end of the week than we did at the start.
I would soon regret this....

### R2D68 Start of the 2 week Engineering Project
It was with some trepidation that arrived onsite for the announcement of the new teams.
I was pretty darn lucky though and we moved through planning to ticking off tasks at quite a rate.
The challenge is to create a facebook rival in Ruby on Rails, a wholly new framework for us all. 

### R2D67 Bank Hol Monday - Weekend Challenge Extension
My sketches and prep from last night work wonders for my productivity today.
I felt like the whole MVC architecture made sense and I was able to piece my code together with feeling as though I was lobbing matchsticks in the air for a game of pick up sticks.
The api remained somewhat of a mystery to me so I pretty much copied that from CLPayne and amended for my slightly different structure.

I've got to the end of the day with a functioning headline generator. I need to action the single page functionality by use hashchanges etc but I may have to leave this for later as I want to run through the Ruby on Rails tutorial.

### R2D66 Weekend Challenge - News Summary
I spent most of the day trying to refine the Notes app challenge while I was trying to get to grips with the flow in a single-page website. I felt this might be more useful than bombarding the Guardian api while I tried to fathom out what the heck I was supposed to be doing. I have set up a homepage for my newsfeed but now I need to get to grips with JSON and other delights. I wonder if a smallish G&T would be a help or hindrance.

![gin pic](http://whatapalaver.co.uk/wp-content/uploads/2018/08/img_5045-2.jpg)

Well, as it happens, the gin didn't hurt too much. I spent much of the evening reviewing single page architecture and sketching out what my news app might look like. I came across a rather [perfect medium blog](https://medium.com/@patrickackerman/classic-front-end-mvc-with-vanilla-javascript-7eee550bc702) on the subject and feel I can now retire for the evening with a colourfully sketched out plan and a greater understaning of MVC.

### R2D65 Weekend Challenge Time
I'm still trying to catch up with the weeks pairing challenge and juggling DOM tutorials. I feel like I get it but everytime I try and put it into action I flounder.

### R2D64
Finally started the notes app and practised using javascript to control the DOM. My struggles throughout this week are going to seriously hamper my chances with the weekend project.

### R2D63
Today was a revelation...
Two hours sitting with a coach and going through some of my current mind-blocks: objects, properties (that are also functions), IIFE, module pattern, exports. If I could just bottle that feeling of comprehension I had at the end then I think I could sail through the rest of the course in contentment. 

I spent the afternoon trying to recap some of the morning enlightenment and felt happy enough with the testing framework progress to move on.

### R2D62
More fumbling in the dark corners of javascript. Puzzling over the multitude of ways to write a JS function and never quite stumbling on the right combination of characters to get the darn thing to work. Fortunately I was paired with someone who had a bit of a grasp today and I managed to come away with a few wins: how to style the terminal console and one example of a working test.

I spent the evening reviewing javascript control of the DOM.

### R2D61
Today was another bad day with javascript. We are supposed to be creating a web app without the use of frameworks or libraries and have started with test driven development without Jasmine or equivalent. That requires us to recreate a test framework in Vanilla JS. I have just about managed to create something that works in the console but attempting to get that info onto a web page - perhaps a page that shows all the tests in one go - is just an horrific prospect.

It appears to require me to know about the DOM and how to access elements. It feels like the stuff JS was made for but somehow I have managed to bypass the actualJS mind-meld that my colleagues seem to have absorbed.

Truly out of-depth, overwhelming and despairing feelings are taking over again......

### R2D60 Monday - Week 7 Makers
We are spending a week reinforcing our very shakey knowledge of Javascript. 

### R2D59 Weekend Challenge  
This was a particularly tricky challenge as the logic behind ten pin bowling is deceptively complex. I initially went down the route of manintaing a frame and roll history that worked very well until I had to handle the final frame scoring. At that point my code expanded to about double the original lines and I decided there must be a more efficient route. Enter Uncle Bob and the bowling kata. Two solutions are presented in the repo. [Bowling Scorecard](https://github.com/Whatapalaver/bowling-challenge). No time to produce a GUI which is a shame.

### R2D58 Friday Wk 6
The first challenge today was to understand promises sufficiently to get an output of our query to the database. We thought we also had to suss out database pooling but in the end we got around that by creating multiple connection clients. I don't entirely understand that but I suspect it is not ideal. We also threw out the EJS templating engine in favour of Mustache, for no better reason than I was following a tutorial that used it. Changing the techbase is easy enough to do but creates much more work than you would expect - in this case all our views had to be renamed and redirects updated, we also had to fathom out how to reuse the EJS partials. So, loads of problems today but we worked together well to tick some of them off and have a huge list a questions yet to be answered/understood. 

### R2D57
I was a bit nervous this morning about how the compromising would work with th eongoing group task. In the end it proved to be a non issue, as we all aligned with tasks that suited us. I ended up working on the unit tests and a series of JS frustrations. We spent hours randomly adding JS snippets in the hope that eventually we would hit upon working code. Rather like the monkeys attempting to recreate the complete works of Shakespeare. 

In the end we engaged the help of coaches who were fantastic today and introduced us to a variety of JS horrors like: promises, asynchronicity, node vs browser JS. I wanted to stick my hands over my ears and shout lah, lah, lah but some of it slipped in and settled in my cortex. I think I may gradually be 'getting it'. I have confidence that tomorrow we will be able to return some actual SQL code rather than just a pending promise.

There's a tiny bit of me that is starting to like this monster called javascript.

### R2D56
I missed yesterday’s update of the groupwork progress but the big win of the day was figuring out how to automate the DB connection and setup with a Jake file. That made me very happy. 

Today in contrast, was shit. We did our Agile standup session this morning, and planned the day, allocating tasks out. By mid-morning it had become clear, that sub-team A had discovered all my tasks were dependencies of their own task and so had just rattled them off before moving on to more exciting stuff. 

My morning was cast asunder - to a wasteland of thwarted efforts and a gazillion merge conflicts.

Life did pick up in the afternoon following an emergency retro and realignment of tasks but I think we have much to learn on team work and task optimisation. 

### R2D54 - Monday week 6 Makers.
Today marked the start of our first group project where we are tasked with the creation process - an AirBNB clone. The main challenge though is the development of “working together” skills. 

We are following the agile approach, which involves morning standups and evening retros. Our focus is on shared team goals and learning! AirBNB will be a lucky side plate. 

I was lucky in the group draw. 4 people from the cohort were absent for the first day and therefore an immediate training burden on the rest of the team. We had a full complement and each member seems to have a similar high level of commitment which helps to keep the strife levels low. 

Tech problems are high so far. We have opted to run this in JS with node, express and PG and spent an inordinate amount of time installing and connecting. The database connection is not up and running yet and I have concerns.....

### R2D53
In the interest of getting upto speed with JS, I spent much of the day powering through the TreeHouse course on Javascript. Juggling instruction in ES6 while coding in ES5 is tricky....
By 6pm I felt ready to finally start digging into to the logic of the coding challenge. Not a huge amount of progress made.

### R2D52
Today marked the start of the Bowling Scorer challenge which required considerable cogitating on the rules of tenpin. Determining the user story was quite tricky. Configuring ESLint to deal with the ES5 version of javascript that we use at Makers was even worse and don't get me started on the hours wasted trying to get Jasmine to communicate with my src files.

### R2D51 - Friday week 5 Makers. 
We had a workshop to discuss callbacks in JS and ended up covering some debugging and flow  monitoring using console.log()
In the afternoon I went back to basic Ruby with exercism and then got slightly derailed by the 99bottles of beer challenge (Sandi Metz). That challenge did not help my confidence levels as I was stumped on the first test which required me to return a string across multiple lines. FFS. Why is that so difficult. I learnt about <<~DOCSTRING

Interesting, but really ugly. Alice saved the day by showing that I could use .join with a “\n” newline character as the join. 

Also had an inspiring conversation about futures that left me thinking that I might be able to explore my interest in data mining, machine learning and AI. Cool stuff!  

### R2D50
I started working with [exercism.io](https://exercism.io/) today. I don't feel particularly confident in either Ruby or JavaScript at the moment, and as we actually do very little language practice at Makers, I thought I'd use this for morning practice.  
I found it pretty difficult to set up the CLI and then submit a basic "Hello Worl" solution so it doesn't bode well for my ongoing language development.

### R2D49
Great pairing session today using the ping pong method. Where we each set a test for the other to pass and rotate. 
We started on the javascript thermostat challenge which will hopefully develop a GUI before the week is up. 
Getting used to a new testing framework (Jasmine) while getting used to the intricacies of JS is interesting...

### R2D48
Taking the learning of new languages to an all-new level today. Rattling off the codewars FizzBuzz kata in JavaScript, Coffeescript and Python. The latter two are much, much more appealing than JS! Attempting the same challenge in Haskell sent me into a tailspin and I decided life was too short or at least my bootcamp experience wasn't long enough to support this learning curve....

### R2D47 - Monday Week 5 @ Makers
It's the start of javascript week and I am nervous. Feels like we are starting from scratch again. So far it hasn't actually proved to be too bad although addition is odd in JS and I cannot be doing with brackets and semi-colons! (){};
***ks ****!

### R2D46
Still on the weekend challenge to recreate twitter. I'm learning some debugging skills as my program is riddled. I'm learning stress avoidance tactics like swinging in the hammock while trying not to go insane. On a more positive note I have also implemented a sign up feature with encrypted passwords.

### R2D45
I started the Chitter Challenge today and went to bed at midnight with the most irritating database connection failure that I just couldn't fathom. Deep frustration. I did manage to set up the whole sinatra, PSQL, capybara stack in record time though.

### R2D44 - Friday Week 4 @ Makers
Struggling to use PATCH im my app.rb rather than just POST and GET. At least I got to learn about forking on GitHub so I could roll back to square one without losing everything.

### R2D43
Mostly assisting other with their code today but that helped to cement my knowledge of testing vs production environments. Also learnt some cool debugging techniques. Get visibility. Tighten the loop. Save_andOpen_Page really helps in capybara.

### R2D42
Loads of progress made with the bookmark manager today.

### R2D41
More work on the Bookmark Manager today. We dealt with the setup of multiple environments so we could have a test one for running our RSpec and Capybara tests - without this the tests risked failing if we were expecting to see a specific URL which had been deleted by the user in Production.
I messed up my code with a Environment = 'Test' rather than Environment == 'Test' and took me a while (with assistance) to fathom. Learned a new trick of riddling code with p to print to the server console.
Also, installed Sinatra Flash which we should be able to use to pass messages to the view.

### R2D40 - Monday Week 4 @ Makers
Today we start on database integration, which I am really excited about.
The weekly challenge is to create a [Bookmark Manager](https://github.com/Whatapalaver/bookmark_manager) based on a Sinatra framework with connection to PostgreSQL. I love SQL!!!
We whizzed through th eafternoon setting up the infrastructure and the connections.

### R2D39
Finished the Rock, Paper, Scissors web app. It was a pretty good challenge, particularly the annoyance of trying to get variables to pass between elements of the program.

### R2D38
Start of the weekend challenge - Rock, Paper, Scissors web app.
I got all the implementation stuff done before I realised I'd left my macbook charger at Makers! I ended up spending the day on the main computer just reminding myself how flexbox works and prepping the style sheets for when I was able to start back on RPS.

### R2D37
Still working on Battle. I've implemented the computer opponent functionality but I am now mixing the control in the view (erb files). I'm going to have to seek some support with that to find a different solution.
I've sussed out how to link the erb files to an external stylesheet. This [Medium post](https://medium.com/@kerenlerner/how-to-include-images-css-and-or-javascript-in-your-sinatra-web-application-45e2ebbfa75f) helped.
I have some styling, but nothing to write home about....

### R2D36
More work on the Battle web game. Mapping out the flow between POST and viewable GETs. Now its time to add some true game play functionality - at the moment the first player always wins, which is a little tedious for Player2. I also need to fathom out what the global variable crime is - my code is littered. 

Struggling to model the exact flow I'm after. I'm trying to have the option of a computer opponent and therefore need to automate their play. It seems that I can't redirect to a POST method, so would need some form of user interaction eg. button press to trigger the computers move. That doesn't sound ideal.

### R2D35 (25th July)
Continuing with Battle. Separating views (erb files) from control (app.rb) and the model (ruby classes and methods within lib). I'm wondering if this is the MVC concept in action?

### R2D34
Started work on the [Battle challenge](https://github.com/Whatapalaver/battle). A game of attack built on Sinatra with Capybara for testing web based features.

### R2D33
Start of Makers week 3 and the introduction to web. We were building our first form with sinatra.

### R2D32
A full day of frustrating coding today, continuing with the Takeaway Challenge that I started yesterday. The idea was to create an order from a menu of available items and to use the twilio api to send a confirmation text message.
I decided that the api implementation was key to the challenge and so moved to that when it become clear I could spend the whole day messing with hashes. I learned how to use ENV variables with dotenv and also how to delete GitHub history after I discovered I had shared sensitive information online.

### R2D30
This is the end if week 2 at Makers. I’ve managed to miss a few days of logging but coding was happening at pace. 

Today we spent the pairing session discussing a very tricky stage of the Oyster card challenge. it was class xtraction and the handling of penalty fairs for edge cases. we discussed loads and tied ourselves up. 

After a break I was able to see we were on track and a little tweaking delivered me a working model. 

I have a few things left to tweak now but it was a good result. 

### R2D27
We had a session on encapsulation this morning and then went onto the [solo skills challenge](https://github.com/Whatapalaver/secret_diary) to prepare a single class SecretDiary app and then split it into multiple classes using the principles of single responsibility, all using TDD of course. This was really useful for me as I'm still pretty nervous about the communication between methods across classes. 

More pairing on the Oystercard challenge this afternoon.

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
