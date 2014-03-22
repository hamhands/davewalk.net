---
layout: post
title:  "PHL Crime Mapper"
date:   2013-01-14 07:33:00
categories: PHL Crime Mapper app deploy open data crime Leaflet
---

Last month the [City of Philadelphia released
data](http://opendataphilly.org/opendata/resource/215/philadelphia-police-part-one-crime-incidents/)
on Part I (violent and serious property) crimes over the last six years.
Today I’m releasing a web application that uses that data to help folks
visualize these crimes in their area: [PHL Crime
Mapper](http://www.phlcrimemapper.com/).

On a computer (non-mobile device), the application allows users to
select a time frame and draw a polygon around the area that they want to
view the crimes for. They can then toggle on/off different types of
crimes and can always change their data range or start over again.

On a smartphone, users select either a 3, 5 or 10 block search area
(approximate) around their location. A tablet version is coming soon,
for now the app should be pretty worthless on iPads and the like. It was
important to me that there was a version of this app that worked on
smartphones and that it was just not the desktop version shrunken down.

The ultimate vision with this is to allow users to select the region
they want to know about and get a text or email alert weekly/monthly of
all the new crimes in that area. It’ll take some time to get there, but
I think the app really becomes useful at that point.

I showed this to my friends over the weekend and one of them asked what
the objective is. I don’t really have one and I don’t know how people
will use it specifically. If they’re like me they’ll draw a polygon
around their house to view the recent crimes in their neighborhood.
Perhaps they’ll change the data range to see how crimes have changed
over time. To me the more you know the better, especially when it comes
to crime in your city and the Police Department thankfully releasing
this data lets it to happen.

It was fun working on this project and I’m pleased with the results for
now although there are some UX and loading time improvements that have
to be made. This was the first time that I got to work with
[Leaflet](http://leafletjs.com/) extensively, which is 100% awesome.
There were a few steps along the way where I thought that I would be
stuck because Leaflet has a smaller API than other client-side mapping
libraries, but it always had the perfect solution. Where Leaflet cannot
offer the functionality there are some great plugins that give you more,
including the awesome [Leaflet
Draw](https://github.com/jacobtoye/Leaflet.draw) that I am using here. I
may have to post again later about Leaflet. I have always been a fan of
the ‘Toner’ basemap from [Stamen
Design](http://maps.stamen.com/#toner/11/40.0020/-75.1180) and I finally
get to use it here. Overall the app is pretty fast once it’s initially
loaded, due to the fast Esri REST server that I’m calling for the data
(and geometry services) from and the markers being [Font
Awesome](http://fortawesome.github.com/Font-Awesome/) CSS sprites.

I hope folks find this useful. [The code is up on
GitHub](https://github.com/davewalk/phl-crime-mapper) and pull requests
and new issues are welcome. It’ll be interesting to see how people use
it and I’m definitely open to making changes to make it more useful and
easier to use.

