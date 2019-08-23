Whatapalaver's 100DaysOfCode Log - Round 4
===

I've been in my first developer role for about a month and it's clear to me that I am going to have to take my journey to "hot shot professional coder" as seriously as I took the bootcamp experience. I can't afford to drift through the experience and instead need a defined developer's development plan to work through. Something like this [fine roadmap](https://github.com/kamranahmedse/developer-roadmap).

So, with that in mind it's time to kick start Round 4 of 100daysofcode to document the progress and keep me accountable.
My previous accountability rounds are till available here:

- [Round 3](https://github.com/Whatapalaver/100_Days_of_Code/blob/master/r3-log.md) documented the 70 days post Makers graduation where I consolidated the bootcamp experience, completed a stack of technical tests and finally secured myself a couple of job offers before accepting a fullstack role at The V&A.
- [Round 2](https://github.com/Whatapalaver/100_Days_of_Code/blob/master/r2-log.md) covered the 99 days of my Makers bootcamp experience. From the pre-course to graduation day.
- [Round 1](https://github.com/Whatapalaver/100_Days_of_Code/blob/master/r2-log.md) This was my initial foray into 100 Days of Code.

RD44
---

I went back to the SQL drawing board today as I found it just too mind boggling to fathom out Rails 5 ActiveRecord syntax for named scopes. I thought it might be easier to get things working with SQL and then do a direct translation. Although there is a google translate equivalent for SQL to ER (scuttle.io) I wasn't convinced with the output. Anyway, I eventually got some syntax for finding objects with images (with_images) and those without (orphaned). Unfortunately the first with_image query won't give me DISTINCT records and that is [apparently tricky in ActiveRecord](https://pdabrowski.com/blog/rails-order-with-distinct), at least in the context of SCope. Ugghh.

```ruby
scope :orphaned, -> { left_outer_joins(:media_items).where('enhanced_object_media_items.enhanced_object_id is null') }
scope :with_image, -> { joins(:media_items).where('enhanced_object_media_items.enhanced_object_id is not null') }
```

RD43
---

Much Rails fun today. Managed to avoid a React rabbit hole by restricting a render json statement with the use of a named scope in the model. Great bit of teamwork today meant that I was able to bring a whole series of workflows together in my head. And such a neat solution. Also got fairly embroiled with some controller rendering to catch some edge case crashes but that was much less fun. I did fathom out how to have [multiple render statements in a single action](https://blog.arkency.com/2014/07/4-ways-to-early-return-from-a-rails-controller/) by the use of `and return`. 

RD42
---

Fixed the timeout issues by:

1. Performing a Net::HTTP head request rather than a full GET request - I only needed to test for a HTTPOK response
2. Using .start() and .finish to open and close an http connection, so that I could loop through all the image checks without having to open and close for each one

That's a great learning experience and for once I found the [Ruby docs](https://ruby-doc.org/stdlib-2.6.3/libdoc/net/http/rdoc/Net/HTTP.html) to be pretty useful when I finally persuaded myself to read them.

This afternoon I'm going to get my head around memoisation - which sounds like another performance hack I need to get familiar with.

RD41
---

Still trying to wrap up a branch that I've been working on for months. Testing on the AWS servers with mega tonnes of data (technical term) has led to no end of performance headaches. Today I've been trying to minimise the number of calls to a method that tests the accessibility of image urls. Despite 4 refactor attempts I'm still plagued with timeouts.

R4D40
---

A major rebase of a 3 month branch lead to new git tricks. I didcovered the interactive rebase mode where you can squash and rename commits.

R4D39
---

Loads of Rails learning today. Putting my code to test on mega data (1.2m+ objects) revealed no end of performance issues. I had to fathom out how to get console logging messages onto AWS Cloudwatch (which is not the most intuitive of interfaces) so I could attempt to debug. Also learned that assigning a db query to a variable eg @results does not save the result, only the active record relationship, and referring to that variable just re-runs the db query.  Adding `.to_a` at the end ensured my results were saved as an array and stopped excessive db calls. I also got into some nitty gritty jsonb querying syntax but its so ugly I can't bring myself to document it. Also, some more migration rollbacks and indexing practice on json fields.

R4D38
---

Learned more about the asset pipeline in Rails and fixed the rails-ujs issue by ensuring it would be wrapped up in the webpacker process. Experimented with markdown static site generators and plumped for [MkDocs](https://www.mkdocs.org/) which so far appears to do everything I need, which basically means it automates the navigation production and combining that with awesome-pages gives me the nested, foldable sidebar that I desire.

R4D37
---

Our lack of rails-ujs reared it's head again. It's one of the hidden magical elements of rails and without it you will pull your hair out wondering why things like link_to and confirmations don't work. 
Useful links: [rail-ujs missing](https://stackoverflow.com/questions/57181467/rails-asset-pipeline-removed-how-to-replicate-rails-ujs-helper-methods) and [rails j-query magic](https://stackoverflow.com/questions/7465919/rails-link-to-method-geting-when-it-should-delete)

Also discovered some whizzy magic in a form_builder with a method that reaches into the class model to retrieve length validations that then get converted to javascript form field length counters. Ooh ahh.

R4D36
---

Got to wrestle with skip-worktree in git again while I continue to struggle with maintaining local variants of config files. Also getting my head around schema.org

R4D35
---

I've been mentoring some of the early stage Ruby challenges on exercism.io I find it surprising how many different iterations are possible and it keeps me on my toes. Today I was reminded of the splat operator.
I also did a bit of my Rails portfolio and experimented with scope definitions and setting defaults after_initialize.

R4D34
---

Today I got to deal with some meaty Git issues as one of my commits had been reverted and it seems there is a whole workflow related to reverting reverts. I had an interesting historical interlude while I read an article by [Linus Torvalds](https://github.com/git/git/blob/master/Documentation/howto/revert-a-faulty-merge.txt) and this nicely illustrated blog on the subject of [reverting git reverts](https://blog.theodo.com/2016/11/revert-the-revert-and-avoid-conflicts/).

In the end my process was:

- `git checkout master` 
- `git pull origin master` this is the branch that had my suspect commit and the revert
- `git checkout suspect_branch`
- `git rebase master` my suspect branch now has the revert applied (see git log)
- `git revert SHA_of_original_reversion`
- Correct the suspect branch, commit and push
- I can now repeat the pull request and all commits should be applied

R4D33
---

I'm not very well at the moment but I'm trying to maintain the learning spirit by working through a [Rails masterclass](https://github.com/Whatapalaver/rails_portfolio) from Udemy. I've implemented friendly_id for creating parametised slugs and used custom routes to implement a status toggle feature for blog posts. Also just finished off the [scrabble_score challenge](https://exercism.io/tracks/ruby/exercises/scrabble-score/solutions/485cc97dd82c4d0cb85f069fb50039e8) at exercism.io where I learned some cool stuff like using merge to create a hash from an existing hash but adding a default value, also how to use a variable in a regex expression.

R4D32 6th Aug
---

I had a tricky challenge from the legacy code base today involving Sir Trevor, custom react components, some custom vanilla js and a load of rails functionality. I was ready to start weeping just before lunch but then we tried 3-way pairing to bounce ideas, then down to solo experimentation and back to pairing. The problem was cracked within 60 mins and by the end of the day I'd fixed 3 Sir Trevor blocks and submitted my PR. To think I was once dubious about pairing!

Also reminds me of this great new video series showing how an [experienced developer might approach a challenge with an unfamiliar legacy code base](https://www.simplybusiness.co.uk/about-us/tech/2019/07/working-with-legacy-code-e01/).

Huge Hiatus......
---

I've probably been away for about 4 months as I felt a bit awkward writing about work stuff everyday but looking back that seems to be a bit of a shame as it means I've lost quite a few of learnings from that period and there have been loads.

So I'm now I'm back, about a week after my 6 month work anniversay and I'm going to try and resurrect near daily learning notes. My focus areas have shifted slightly with now more focus on becoming super proficient at Rails and also learning Python so I can be a nifty scripter.

R4D31
---

Today's head banging moment was courtesy of webpack. Perhap's it was making me suffer because I came into work wearing my parceljs t-shirt. I'm juggling three projects at the moment and all of them are falling over because of webpack config issues. I think I've solved two after reading the following helpful blogs. The last one has too much black magic imported via node_modules for me to totally fathom.

[Beginner webpack](https://medium.com/javascript-training/beginner-s-guide-to-webpack-b1f1a3638460)   
[Slightly more advanced webpack](https://medium.com/@rajaraodv/webpack-the-confusing-parts-58712f8fcad9)  
and also this link which explained how my last project was managing to [auto-generate an index,html](https://medium.com/a-beginners-guide-for-webpack-2/index-html-using-html-webpack-plugin-85eabdb73474), seemingly by magic:

R4D30 
---

Web components galore today. I was focussed on raw web components which were probably ok but I had significant webpack issues which made it pretty tricky to test.
Finished the day with Styled Components in React but also managed to fix a hosting error I had on netlify as a result of me not really 'getting' SPA and url paths as well as perhaps a bit of server vs clientside confusion.
I'm still confused but this blog helped, [File not found on netlify](https://www.slightedgecoder.com/2018/12/18/page-not-found-on-netlify-with-react-router/)  

R4D29
---

I was set a 'trivial' challenge of creating a mini react app to exploit the zoomable power of IIIF. It was deemed trivial as I was building on the shoulders of others but in my limited experience, nothing is ever trivial. I spent the entire morning battling with yarn trying to install a gazillion dependencies that had version conflicts, multiple dependencies deep. This is a total frustration...

I spent the evening at the ReactJS bootcamp where we were starting from scratch and building CRA app to exploit an image api. It proved to be a welcome confidence boost and I learned quite a bit about routing and even materialui which I'm not a major fan of yet.

R4D28 
---

I'm exploring web components today. I love the concept of componentisation without the ties of a framework / (massive React library) but I am struggling to get to grips with the syntax. I'm hopping between native components and those built with lit-element and that is probably adding to the confusion.

R4D27 24th Mar
---

I had a very brief session of coding today, working through a recent intro to Python course on FEM.

R4D19-26
---

I haven't logged consistently this week but its all been Elasticsearch but also two session with reactJS. 

R4D18 Saturday 16th Mar
---

Homework time today for the React bootcamp. I was refactoring the facebook messenger app. Again everything is crammed into app.js. I discovered a cool little extension for VSCode that lets me write out a stateless functional component just by typi sfc and a class component with cc. Total genius.

R4D15 - D17
---

All python and elasticsearch. Mainly frustrations with a modicum of yay!
Thursday was day 2 of the React bootcamp where we refactored a React app with everything crammed into app.js

R4D15 - Tue 12th Mar
---

I had a long weekend away from code. 

I managed to setup a Flask app to integrate with my Elasticsearch instance running on localhost. it outlined the need to do some basic python lessons as I had a bugger of a job trying to perform a substring operation within a jinja template. I was trying to force a JS function but of course every language has its own special way. 

Today was the first night of the React bootcamp I arranged yesterday. 
Tonight was ES6 and JavaScript features. Very useful actually and I coped well because of the Frontend Masters (Functional JS) course I’ve been doing on my commute. 

R4D14
---

I spent some time on a vanilla JS project to showcase a stereogram from our collection. I called it Wiggle Moon as I’m experimenting with a 3D wiggle. It’s pretty simple but I wouldnt have been able to do it before I started the Wes Bos JS30 course. 

In the afternoon it was back to Python and my attempt to create an elasticsearch interface. 

R4D13
---

Everytime I try and setup a Python dev environment I end up in a whole heap of poop! It was going relatively well today, I sorted the $PATH bit that normally confuses me and even set up Virtualenv but I ran into headache zone when I tried to clone a repo into a virtualenv and then lurched from one head bang to the next. By the end of the day I had finally set up my environment with a Vagrant box and an Elasticsearch instance so I could quickly race through some exercises from the excellent Relevant Search book by Doug Turnball and John Berryman. At least I'm in a good place to crack on tomorrow.

R4D12
---

Found a great tool for testing custom ES analysers and then discovered its now broken for the latest version of ES. That took quite a few hours of hairpulling and Stack Overflowing but I had the bug confirmed. I then discovered the more manual but still useful \_analyse with explain: true which just about saved the day.
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
