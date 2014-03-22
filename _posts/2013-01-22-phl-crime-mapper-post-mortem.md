---
layout: post
title:  "PHL Crime Mapper Post Mortem"
date:   2013-01-22 00:22:00
categories: PHL Crime Mapper app crime post mortem open data
---

It’s been a little over a week since I released [PHL Crime
Mapper](http://www.phlcrimemapper.com) and the response has been beyond
my wildest dreams. Here’s a few select quotes that made me proud:

["…a handy
tool…"](http://www.philebrity.com/2013/01/14/theres-an-app-for-that-phl-crime-mapper/)

["…gives easiest look yet at crimes by
neighborhood"](http://www.philly.com/philly/news/breaking/New_website_gives_easiest_look_yet_at_Philly_crimes_by_neighborhood.html)

["…wins points for
simplicity…"](http://technicallyphilly.com/2013/01/15/phl-crime-mapper-app)

["…nifty…"](http://blogs.phillymag.com/the_philly_post/2013/01/15/phl-crime-mapper-documents-citys-pain/)

["…handy interface for seeing where serious crimes are being
committed."](http://www.newsworks.org/index.php/local//onward/49541-phl-crime-mapper-open-data-in-action)

["…crisp, easy to use…the simplicity and refinement of design is
excellent."](https://twitter.com/greenperspectiv/status/291251453278949376)

[I was even on the radio to talk about
it!](http://philadelphia.cbslocal.com/2013/01/20/philadelphias-serious-crime-database-gets-makeover/)

I like seeing words like “handy” and “simplicity” because that’s
definitely what I was going for. The app strives to do one thing and
hopefully do it well.

I also got a lot of feedback by email from community leaders and others
about how they found the app useful. I didn’t think of it before, but
this would be really helpful for community organizations and
neighborhood watch groups. I’ll have to think about ways to get the word
out to them in the future. Overall so far I’ve gotten a lot of feedback
that has solidified how I should move the development forward.

A few things have been identified that need improvement. Some users had
issues with using the application in so far as drawing an area and
changing the date range. So tonight I added a “Draw” button to the black
box on the left that explains how to use the app. In the process I
actually decreased the height of that box by removing some copy from the
last sentence. So that’s good.

The other thing that I have to work on is finding a date selector that
is easy to use. I really like the [current
one](http://ghusse.github.com/jQRangeSlider/) but I’ve actually
witnessed myself a few people having trouble figuring out how it works.
I may find a different one (although I hate the calendar picker ones) or
at least put a hover over the slider that explains how to use it.

Beyond that I’ve thought about some long term bigger additions that
could really make the app awesome. I also have to work on making sure
the codebase remains maintainable by using Backbone and maybe porting
the JavaScript to CoffeeScript. I’ve never used CoffeeScript before so
this would be a good way to learn.

Finally, some closing stats:

-   30% of visits from mobile devices (including tablets). This number
    was a bit surprising to me, but it shouldn’t be. There was a mobile
    version but a healthy amount of these hits were on tablets, which
    the app currently doesn’t support at all, which has been been
    driving me crazy. I have to spend some time soon adding that
    support.
-   The app was viewed in 46 states and 54 countries (whoa)!
-   Internet Explorer, Chrome and Safari split 70% of the traffic down
    the middle, Firefox got 16% and a bucketful of other browsers got
    the rest. Great to see Internet Explorer not in the lead.
-   Most toggled crime: Thefts. Which makes sense because there are so
    many of them.
-   [The Philly.com
    article](http://www.philly.com/philly/news/breaking/New_website_gives_easiest_look_yet_at_Philly_crimes_by_neighborhood.html)
    accounted for about 63% of traffic, which is amazing. Interestingly
    enough, a fifth of that came in through the mobile version of their
    website.

The traffic has died down, so now it’s time to get back to work on
making the application better long term.

