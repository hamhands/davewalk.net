---
layout: post
title:  "Introducing YOWATER"
date:   2014-07-20 17:10:00
categories: Yo, app
---
I'm intrigued by the new "social network" Yo, [as I previously wrote about](/2014/07/04/yo.html), and today I finished my first YO app. It's called [YOWATER](http://yowater.net) and it helps you keep track of your water intake. When you drink a glass, send a Yo to **YOWATER**. To get your intake over the last 24 hours, go to [yowater.net](http://yowater.net) and search for your username. Very simple.  

Simple, yet useful, to me at least. I sometimes forget to drink as much water as I should and it's annoying to input into another app. With this app I'm esssentially using Yo as a button with which I can log something. The Android app allows me to create a widget that with one push will send a Yo to username, which is perfect for this. And I think the results page is pretty neat with how the blue fills up the screen with each glass that you drink.  

It would become more interesting if the app could Yo you back if you haven't had a glass of water in a configurable period of time. Currently this isn't possible since there's no way for the app to ensure that you are the user that you say you are, but if the Yo were to add something like OAuth2 so that users can confirm their identity on the website, I would add reminders as well.  

Overall a fun little project that took me about six hours to make (most of it on the CSS styling) thanks to Heroku, ExpressJS, Jade and MongoDB. It'll be interesting to see if anyone uses it.