---
layout: post
title: "HTML & CSS Reading Group 2"
date: 2013-03-18 15:50 -06:00
comments: true
sharing: true
permalink: /2013/03/html-and-css-reading-group-2
tags: [gSchool, reading group]
---

It was really interesting for me to read the CSS portion of this book - I've never had any experience with CSS before, and it's interesting to see all the design elements you can implement with pure CSS alone.

I tried to experiment a bit with updating my blog, but had limited success - I think part of it was that the layouts were written in haml, not HTML, which I would have found really helpful in modifying, saying, a .panel class.

Most of what I did (I had previously already tweaked the colors of my blog) was with trying to manipulate the title bar a bit.  I'm still not super happy with it, but I can fiddle around with it later.

Here's what it was:
  <img src="https://s3-us-west-2.amazonaws.com/ebdrummond.com/images/ss1.png" />


And here's what it is now:
  <img src="https://s3-us-west-2.amazonaws.com/ebdrummond.com/images/ss2.png" />

with code:

```html
    h2 {
      font-size: 40px;
      letter-spacing: 0.06em;
      word-spacing: 0.06em;
      text-shadow: -1px 1px 10px #704111;
    }
```

Again, really not to happy with it, but more to come soon!
