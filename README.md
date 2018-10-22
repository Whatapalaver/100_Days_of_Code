
Whatapalaver's 100DaysOfCode Log - Round 3
=======

This is the log of my third #100DaysOfCode challenge. 
I cut [round 2](https://github.com/Whatapalaver/100_Days_of_Code/blob/master/r2-log.md) short on Makers Graduation - day 99 (sacrilege?) and restarted round 3 on Saturday after Makers graduation.

Check out [the Official Site](http://100daysofcode.com/) for the #100DaysOfCode movement.

***Exciting News***
-------
I'm now combining my 100DaysofCode journing with Instagram, see [Whatapalaver Codes](https://www.instagram.com/whatapalaver_codes/) for additional visual excitement of a coding nature!

## Log

### R3D23
Well I had a lot of fun today with heroku again. Having decided not to use create-react-app for my react frontend build I was then left feeling a bit unsupported when I couldn't get Heroku to host any of my frontend. Hours of researching parcel documentation (replacement for webpacker) and eventually I fathomed out that the build was stored in dist and not build.... Any, I do now have both the frontend and backend API on Heroku. It's spread across odd branches as Github has been misbehaving for hours today. I just need to fathom out tests, do something semi-fancy with my loading tables and then I should be good to go with this tech test.

Tonight I have a meetup where we will build a neural network from scratch.

### R3D22
I spent the day trying to catch up with the coursework from the Machine Learning course I started at the beginning of the week. I'm boiling my head with high speed visualisations of minimising the square of diffeneces. Everything is learned at 1.5x playback speed since Makers.

### R3D21 Saturday 18_Oct
Made loads of progress today. Sussed out how to pass props down to my table component by including it in the parents render function rather than in app.js. Sorted out how to map through my api call to display in the table rows. I've nearly finished the tech test although I still haven't fathomed out what I need redux for and I haven't written any tests. My api calls are painfully slow as well so I must have missed a better approach as its currently intolerable from a user perspective.

### R3D17
This dragonstack course is pretty challenging and I haven't even got to React yet, I need to crack on or else it will be more of a hindrance to my tech test progress. I've been spending a little time on the tech test today, mostly setting up the structure of the backend and pondering how my api should look in order to allow the React app to select specific fields. Do I need multiple api's for each potential field (I suspect that's a no) or somehow pass the field name as a param to the get query. This sounds more likely but also yet another thing that I don't know how to do. In order to feel like I'm making some progress I have set up the program to deliver an api that is currently fixed to show the stats for the education field. At least with this progress I can move onto the frontend communication and styling.

### R3D16
I was issued with my first real tech test today which requires me to generate an API from a DB hosted on AWS and generate a single page website in React/Redux to show a summary according to the selected variable selected. I'm juggling this challenge with a Udemy course called Dragonstack as I think it will prove useful in the React implementation. I'm taking the time to really understand each section of the implementation rather than the time pressured pragmatism of, settling for something that works.

### R3D15
Finished my first post-Makers Rails application [Univ App](https://github.com/Whatapalaver/univ_app). I found it really handy to walk through a professional approach to Rails app execution. I learned a few debug tricks using byebug but also felt far more familiar with the DIY user authentication using bcrypt. It's also the first project where I feel pretty happy with the design of the frontend.

### R3D13
More Rails today and then I had fun unpicking the experiment with haml. I don’t like it. It may be neater but erb follows the rules of html which I already understand, with haml it feels like I have to learn too much syntax. I’ve been writing in erb and converting to haml which isn’t great workflow. 

### R3D12
I feel a little blown by the wind at the moment. Everytime I see a new company that I am interested in, I shift my focus to their current stack. It's a bit like the early days of dabbling with coding when I spent most of my time wondering which language I should start with. At least today I have made some good progress with Ruby on Rails and spent more time focussing on the frontend than I typically have done so far on the journey. I have a neat little app set up that I styled using Google's Materialize (anything to avoid Bootstrap!) and also tried out haml instead of erb for templating.

### R3D10
I've been going loopy with Google Scripts and have now had to fathom a way to export a single sheet to PDF without the need to hide the other sheets. That has led me to the Google Sheets API and a rather neat way to convert a Blob to a PDF. I've set up a new Gist for all things [Google Sheet to PDF Export...](https://gist.github.com/Whatapalaver/4db56950daf84cf1dd2c4765a540e17f) 
Also having fun with Ruby.pow(2) - I feel like a superhero.

### R3D8
I'm back to Conway's Game of Life and loving it. It is tying in nicely with my concurrent studying of Sandi Metz's 99 Bottles of Beer as I have somehow managed to create code with ABC size errors. That's Assignment, Branch, Condition size and means I am forcing my method to do too much. I probably need to read a bit more or risk another question on Stack Overflow.

### R3D6
Spent the day working on a google scripts project. I needed to loop through a product list and create a pdf file showing details for each one. I’ve done something similar in excel before but translating to the javascript google apps language was something new. I’m pretty impressed by the potential within google sheets, I may be about to turn my back on excel. 

### R3D5
Had my first developer interview which turned out to be an analyst role without any development. Shame, as it was a great product and I need to believe in my product. 

Progressing well with Java and I have an interesting natural disaster project brewing with the Makers cohort. 

### R3D4
Scouring NASA APIs today for potential project ideas. Also started the 99 Bottles of Beer refactoring project with Sandi Metz. 

### R3D3
I’m still waiting for feedback from my early Java exercism challenges so I have now added the Kotlin track into the mix. 

### R3D1
So it's Saturday, day after graduation day and I actually have free time and a chance to remind myself what it means to have a family. We went for a walk in the sun and pondered futures.

I'm looking for work now, but I'm keen to make sure that first job sets me off in the direction of an exciting and challenging coding future. I've been scouring LinkedIn for potentially interesting roles and everything that excited me required Java skills. So that's decided. My post Makers month of consolidation requires me to bolster my understanding of javascript and to become pretty adept at Java. It's going to be a fun ride towards challenging employment.

So on Day 1, I've installed IntelliJ Idea and completed "Hello,World!" of the exercism.io Java track. Let's see where this new journey takes me.
