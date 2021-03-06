Whatapalaver's 100DaysOfCode Log - Round 5
===

Round 5 was a big flop. I only recorded 3 days before abandoning the concept. Lets hope round 6 is more interesting.

R5D3
---

I'm back onto many-many relationships again and can't help feeling that I must be making a giant great mole hill out of this stuff. I've got many-many relationships between users and companies. Many-many between companies and addresses and then many-many between addresses and address_types. I'm now experimenting with has_many :through models but feel like I have created one great big mess. Surely it was never this bad with SQL? I'm also trying out BDD with cucumber which has to be cool as it has gherkin syntax.

R5D2
---

The feature I've been working on at work for the last forever (few months) has now been pushed to production and already the teeny tiny bugs are scuttling across the screen. That just goes to show that my tests are not comprehensive enough. Anyway, the latest bug just involved a missing parameter. Logger.debug to the rescue as it helped me hone in on the problematic area.

R5D1
---

My first Rails coaching challenge involves me working with ActiveRecord and setting up some many-to-many relationships which mirror some of the struggles I have at work.
[This blog](https://www.sitepoint.com/master-many-to-many-associations-with-activerecord/) very neatly demonstrates 3 scenarios HABTM, has_many :through and has_many :through :source and [this blog](http://joshfrankel.me/blog/create-a-many-to-many-activerecord-association-in-ruby-on-rails/) is equally useful.

I'm already beginning to see the limitations of HABTM now that I want to add more fields to my join table and need to think about validations.
