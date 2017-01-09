+++
date = "2017-01-09T18:30:00+08:00"
draft = false
tags = ["", ""]
title = "The Clarentine Calendar Explained"
+++

A note on notation: all numbers are in base-twelve unless it ends with a e, which means it is in decimal or base-ten.

The Clarentine Calendar that I recently published contains a number of ... interesting ... systems, the most notable of which is the usage of base-twelve and the ignoring of the conventional 265/365e year.

The reason for using duodecimal has been mentioned by many before me; I will not repeat them again.  If you are too lazy to find out, it basically boils down to composability. 

The reason I didn't even try to incorporate the traditional 265 day cycle into the calendar is because it doesn't matter.  I don't care about needing the calendar to keep track of the seasons for me, which is, as far as I can tell, the main reason for a solar calendar in the first place.  If I needed to know the current season, I can always look out of the window, or in the case here in Malaysia, remain blissfully ignorant of any seasons at all.

I don't care how far along Earth is along its rotation around the Sun; I sleep just as well at night not knowing this information.  A rational system of dividing time matters far more to me.

The other notable feature of the calendar is its usage of _subdivisions_.  Subdivisions exist because of how I structure my life: I have certain tasks that I do every 3, 4, and 6 days, which are perfectly aligned with these subdivisions.  These are the fundamental units of time that I work with beyond the single day; it makes sense to incorporate them into my personal calendar as well.

The choice of the J2000 epoch was arbitrary; it's close enough to my lifetime to have the years in fairly low numbers, and has a nice compatibility with UTC that functions just like the Unix 1 Jan 1970e epoch.

I'm still working on a better way to notate the difference between absolute and relative dates; adding a 'y' in the middle of the string looks ugly.  However, I consider the overall _structure_ of the calendar complete; the naming and some small details might change, but the overall layout of the calendar should be final.