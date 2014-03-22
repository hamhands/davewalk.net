---
layout: post
title:  "Philly Hoods"
date:   2013-09-09 08:40:00
categories: deploy nodejs node API philadelphia philly neighborhood geo postgresql openshift
---

Today I’m releasing [Philly Hoods](http://phillyhoods.net/), a
neighborhoods API for Philadelphia. For now it’s pretty simple: give it
a pair of coordinates in Philadelphia and it’ll tell you what
neighborhood you’re in and give you a GeoJSON representation of the
neighborhood polygon. Or, pass a string and it’ll try to match one or
more neighborhoods to it. Check out [the docs](http://phillyhoods.net/)
for more information and a demo. [The code’s on
GitHub](https://github.com/davewalk/philly-hoods).

It’s a simple project but it was fun to do and like all my side projects
it gave me a chance to mess around with some new technology for the
first time:

**Node.js**: This is my first project in production using Node. I’ve been
messing with it for a while on some larger things (some still in the
works) but it’s good to get something out the door. Again, I’m not
really doing anything crazy here, I’m using callbacks, I haven’t yet
gotten into the promises and all of the more advanced stuff. But I think
Node is ideal for writing APIs and will continue to look to it in the
future for that.

I decided to go with [Restify](http://mcavage.me/node-restify/) over
Express for writing the API and I’m really glad I did. It’s designed
specifically from writing RESTful APIs so it does a lot of the work for
you or makes other things easy with built-in Bunyan support for logging,
throttling and a few other small things that were helpful.

**PostgreSQL and PostGIS**: This is one that I’ve been wanting to dig into
for some time. It’s a database that I’ve messed with but never had to
work with from front to end on a project. It took me a while to figure
out to convert and insert the polygons into a table from a shapefile but
eventually I got it. Once you get the hang of the spatial queries that
you can do with PostGIS you realize that the possibilities are pretty
much endless. It’s kind of addictive. Definitely be using PostGIS again
in the future if a need something spatial.

**OpenShift**: I’ve used Heroku as a PaaS before, but never
[OpenShift](https://www.openshift.com/). I think the two of them are
pretty similar from a workflow point of view (deploying from a
`git push`, what a beautiful thing). What I liked about OpenShift is
that you can actually SSH in to your gear (like a dyno) to get a better
sense of how it works. Some people probably prefer to keep the platform
as a black box but I like the flexibility to poke around a little bit if
I want to. Heroku on the other hand probably has a smoother command line
API to get stuff done but OpenShift isn’t too far behind. Another
appealing feature of OpenShift is [OpenShift
Origins](https://www.openshift.com/wiki/installing-openshift-origin-using-vagrant-and-puppet)
which appears to be a way to run a local copy of the OpenShift platform
for development. This could be a better way to get a local environment
close to what will be run in production than the Vagrant path that I
went for this project. Origins is also how you go about developing your
own “cartridges” (or “add-ons” in Heroku-speak) that you can use on the
platform and even share with others. Open source FTW.

Yeah, so that’s about it. I’m excited to see how (and if!) people use
this API. I’ve heard folks in the past talk about how something like
this would be helpful, so we’ll see.

Now on to the next project...

