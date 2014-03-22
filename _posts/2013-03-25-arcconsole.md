---
layout: post
title:  "ArcConsole"
date:   2013-03-25 20:50:08
categories: JavaScript ArcGIS API console Backbone
---


I just released something that I’ve been working on recently:
[ArcConsole](https://github.com/CityOfPhiladelphia/arc-console "ArcConsole on GitHub").
[Check out a
demo](http://arc-console.s3-website-us-east-1.amazonaws.com/ "ArcConsole Demo").

It’s a simplified, intuitive API console for the ArcGIS REST API. It
uses awesome JavaScript libraries like Backbone, Backbone Forms, Chosen,
Bootstrap, Leaflet and Leaflet Draw to take some of the pain out of
querying data from the standard ArcGIS REST API.

The ArcGIS REST API is really powerful and the City of Philadelphia
(which I work for) is using it more in our open data efforts. We’ve got
some big time datasets on it like all of the Police Dept’s Part I crimes
since the beginning of 2006 and the Office of Property Assessments’
recent actual value initiative which set new values for almost every
property in the city. But, it can be frustrating for developers and
other users that are new to querying the API to get started. This
application attempts to make that on-boarding a bit easier by stripping
away some of the advanced features that we don’t see being used very
often. If the user needs those advanced features, like non-Web Mercator
spatial references, they can use the standard API console at any time.
But with this application the user doesn’t have to navigate to the
service and layer that they need, they just select the data set that
they want from the top drop-down and the rest of the parameters and the
application constructs the URL for them. There’s a static JSON file that
defines all of those endpoints and additional information like a
description and links to metadata can be included as well. Plus the
ability to draw the geometry that you want to query on instead of the
frustration of trying to the object string just right is a big step up
in my opinion.

The app’s still a work in progress and we’ll look to improve it over
time. With some server-side code, it could be extended into a full-blown
data extractor. There’s a lot still to do and you can check out the code
at the City of Philadelphia’s GitHub page.

Adding a repo to the [official City of Philadelphia GitHub
page](https://github.com/CityOfPhiladelphia "City of Philadelphia on GitHub")
was especially satisfying for me. The City of Philadelphia is on GitHub.
And I have some of my code in it. How cool is that?

