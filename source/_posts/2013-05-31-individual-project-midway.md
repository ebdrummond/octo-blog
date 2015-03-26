---
layout: post
title: "Individual Project Midway"
date: 2013-05-31 10:07 -06:00
comments: true
sharing: true
permalink: /2013/05/individual-project-midway
tags: [gSchool, new leaf massage]
---

My feelings upon starting the individual project were a mixture of excitement and nervousness, weighted towards the former.  It was scary to think though - I was hoping through this project, I'd realize I know more than I think I do, but was nervous the opposite would turn out to be true.  I can happily report that, so far, I'm feeling my knowledge is right about where I thought it was.  I'm not the world's greatest gift to programming, but I'm certainly not awful either.

So far, it's been a little bit slow.  I've managed to get to the point where an admin can sign in, search for a client, and create an appointment for the client.  Once the appointment is created, they get a text via Twilio.  This sounds like a lot, but was actually really simple, and I'm working on the hard part now - the logic for time slots and determining which time slots are taken, which are free, and which of the free ones have enough time in them to schedule appointments (if it's a thirty minute timeslot, nothing can be scheduled; if it's a sixty minute timeslot, only the sixty minute massage should show up as an option).

I think once this part is complete, the rest of the MVP will fall into place pretty easily - this is what most of the difficult logic rests upon in the app.  I owe Katrina a huge shout out for her help yesterday.  She helped me to think through how to structure this logic (we have a DayPlanner class, a TimeSlot class, and a Clock class - the last one is because we don't care about the date for a timeslot or dayplanner; only the time), and it would have been a lot messier without her guidance.

I'm also really wanting to use AJAX for some of the implementation on the front end.  I'd love for the admin appointment scheduling to be on one page - admin searches for a client; once client is selected, the date picker pops up; once date is selected, time picker pops up; once time is selected, massage duration selection pops up with appropriate options given the duration of the available time slot.  I really don't know how to do this, so I'm hoping I can get some help from my new mentor.

Speaking of which, I'm really excited to be working with Ashish - just from our email conversations so far, he seems awesome.  We're doing a get to know you call on Sunday, so I'll find out more then, but I'm excited.

I also am really grateful for the help Jim gave me in the previous mentoring rotation.  He was really great to work with and provided me with great feedback when I was starting to go down paths that didn't make a whole lot of sense in my code.

It is crazy to think there's only seven weeks left.  This has felt like a really long four plus months so far, and at times when the stress level was off the charts it felt like the end of the program was eons away.  Now that I'm nearing the end, it's a weird feeling.  I'm excited with everything I've learned so far, and excited to start a new job, but it just feels kind of weird that we're already almost done not that we're at the end.

It is an interesting thing to look back though at where I was a few months ago.  Coming in, I had no clue what I was doing, and for the longest time didn't feel like a real developer.  Now, I'm beginning to feel like I can say with confidence that yes, I am a developer.  I can take a problem, and find a way to implement a real solution.  I still have a lot to learn with new styles and refactoring and need help from teammates, mentors, or instructors, but that's not really any different from where most real developers are in real life - most developers work on teams and get advice and feedback from others too.

I still do have to pinch myself to think how far I've come in just 18 weeks though - this feeling is incredible and I'm so glad I made the leap to restart my life as a developer.  It hasn't been easy by any means, but it's sure been rewarding and I can't wait to see what I'll be doing next.
