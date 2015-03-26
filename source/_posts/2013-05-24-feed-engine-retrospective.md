---
layout: post
title: "Feed Engine Retrospective"
date: 2013-05-24 14:47 -06:00
comments: true
sharing: true
permalink: /2013/05/feed-engine-retrospective
tags: [gSchool, feed engine]
---

Ah - FeedEngine is in the books.  For some reason, this was a difficult project to get through, even though I loved what we were building.  It seems like we've reached a point in the class where a lot of people are feeling burned out, and I think that impacted some of our team this project - we ended up dropping a lot of the functionality that I wanted to implement because we couldn't get through it all with the amount of work the group as a whole was putting in.

At the same time, I learned a lot from this project.  The two things I'm happiest learning about are how to interact with external APIs (Kyle and I implemented the Instagram service, and I implemented the Foursquare service), and refactoring my code to extract logic from the views and controllers, and even the model.  For this, I have to thank Raphael.

An example of refactoring can be seen in our implementation of the logic relating to the user show page.  For this page, we needed to break a user's trips out into current trips, past trips, and upcoming trips, AND we needed to determine whether the trip was private AND we needed to determine, if the trip was private, if the current viewer was authorized to view the trip.  Sounds easy, right?  I really wasn't expecting it to be that horribly difficult, but it ended up being harder than I thought to implement all of this logic in one place.

The way I originally wrote this part of the code, I had current, past, and upcoming trips in the Trip model, and handled the logic for whether the current user could view each trip in the controller.  Raph put a stop to that.  We ended up extracting all of this logic into a UserShow class, which took in the current user and the user whose profile was being viewed, ran through each trip to see if it was private and if the current user had viewing rights, and then split the trips into their correct timeframe.  You can view the final implementation here: [github.com/raphweiner/feed_engine/blob/master/app/lib/user_show.rb](https://github.com/raphweiner/feed_engine/blob/master/app/lib/user_show.rb)

I also learned to place even more value on communicating with your team, especially when you're touching someone else's code.  There were a number of times that I pulled down master to build on code I had previously implemented, and found it had been refactored so much that I had to spend half an hour just figuring out what the heck it was now doing.  Worse, there were times files I had been working on were deleted or the refactoring broke the code I had originally written.  This was pretty frustrating for me, and I'm even more aware now that if you're touching someone else's code, it's a great idea to work with them first.

Overall, I think our project is a good first step, but I wish it went further.  There's a lot more functionality I would like to build out and changes I'd like to made to the front end to make it look sleeker as well.  I'd link to the project, but Jeff is turning off the extra background workers he had provisioned, so the app will no longer work.  I'm taking some time off between graduating gSchool and starting a job, so one thing I'd love to do is to keep working on Kreepr and get it to a place I'm happier with, with more features, more security and background logic, and a cleaner look.

I'm also really excited to be starting our independent project next week.  I don't have 100% sign off yet, but I had talked to Katrina about my idea, and it sounds like I'll be able to do PART of it - my original idea is too large a project to do independently in 9 days.  What I'm going to be doing is making a website for my sister, who is a massage therapist.  Once it's completely done, I'd like to have functionality to let Meghan set her schedule with a base weekly schedule that autogenerates up to two months out, with the ability to go in and tweak individual days.  In addition to a confirmation e-mail when an appointment is scheduled and a reminder e-mail a day or two out, I'd also like to implement text messaging a few hours before an appointment to remind the customer, and let them text back if they need to cancel the appointment.  I'd like to integrate with Yelp to show her overall review count, and maybe recent reviews.  Lastly, I'd like the ability to allow customers to pre-pay for individual massages or massage packages online, and allow Meghan to charge a cancellation fee for missed appointments.

One of the requirements for this project is to build an API and gem on our own, which I think fits in nicely with the scheduling component.  There are a few other gems out there that I found, but none of them have been maintained in the past year; I'd also love if my gem would give back to the community so that other people can use it for their own projects as well.

I'm really excited to be doing this project, for a few reasons.

1. I think the building out the scheduling component will be a pretty difficult, and it's a challenge that I think will be extremely rewarding.
2. I really want to give this gift to my sister.  Not only is she basically one of the most wonderful, caring, compassionate people on the planet and I want to help her grow her business, she also hooks me up with free massages.
3. I'm really glad to be doing this project while I'm in gSchool.  Since this is a site that will actually be used, security is a big concern and I want to be sure that everything is locked down.  It will be really good to have that second set of eyes from my instructors so they can let me know if there are any vulnerabilities that I overlooked.

So, super excited to get cracking on that, but also, not going to lie - I'm excited about the long weekend too!
