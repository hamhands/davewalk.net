---
layout: post
title:  "Did The Cavs Win Last Night?"
date:   2012-12-16 11:05:00
categories: app deploy nba basketball Cavs
---

*March 2014 Update: This app is currently broken due to Twitter's API requiring authentication. I hope to bring it back and better than ever for the 2014-2015 season.*

Yesterday I finished up a little web app that I’ve been working on
over the last few weeks when I got a chance: [Did The Cavs Win Last
Night?](http://www.didthecavswinlastnight.net) A while back I came
across [Is there a Giants game
today?](http://isthereagiantsgametoday.com/) and thought it was a great
idea in its simplicity. I’m definitely a fan of one-purpose single-page
apps because they can be really good at the very one thing that they are
trying to do.

So I created something similar for the NBA that not only tells you when
the next game is, but tells you if your team won the night before. And
not only that, but it’ll give you fresh stories and videos about the
game. I envisioned folks waking up the day after a game to see how their
team did the night before. In the past I maybe went to NBA.com or
ESPN.com to get the score and some single wrap-up, but now with this app
it’s possible to get a bunch of viewpoints in one place.

![image](http://www.didthecavswinlastnight.net/screenshot.png)

The app is entirely static. When a user accesses it it checks if there
was a game yesterday by calling a JSON file of the team’s schedule. If
there was, it’ll ask the Twitter account
[@SimpleNBAScores](http://www.twitter.com/SimpleNBAScores) for the
score. It then pulls up stories from blogs and websites and videos on
Youtube about the game to give a more complete view of what happened and
what people are saying about it.

It was fun to make and it gave me a chance to try out a few new things
like: media queries (pretty simple since this was one column), Canvas
(just one element but quadratic curves can be tricky) and
[Yeoman](http://www.yeoman.io), which I can’t live without now. I also
have it hosted on S3, which is new to me but was pretty easy and working
well so far. Deploying through their web client is a pain, but I think
I’ll try to make a command line application that streamlines that a bit.

While planning this project I did a lot of research into how I can get
sports scores on the client-side and basically there are none besides
that Twitter account. ESPN has an API, but the general public isn’t
given access to scores and you need a key anyway so it wouldn’t work on
the client. All other APIs for sports info are paid. There is one way
person that found a ESPN live score stream and he created RSS feeds to
scrap it, but I couldn’t make jQuery GET requests to it. So there’s
almost nothing, which is strange to me because sports scores are so
ubiquitous. You’d think that it would be in the NBA’s best interest to
put out a robust API, why not, but I guess there’s too much money at
stake. For now I’ll have to use the Twitter feed even though it’s using
a depreciated non-auth version of the API. If that goes down I’ll
probably have to create my own API that all version of Did The… can use.

Anyway, I hope people find it useful. [The code is on
GitHub](https://github.com/davewalk/did-the-nba-team-win-last-night) and
I’ve included instructions on how to setup it up for other teams.
Hopefully folks will fork it and deploy a version of their team!

