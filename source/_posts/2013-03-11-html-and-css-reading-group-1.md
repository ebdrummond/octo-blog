---
layout: post
title: "HTML & CSS Reading Group 1"
date: 2013-03-11 15:31 -06:00
comments: true
sharing: true
permalink: /2013/03/html-and-css-reading-group-1
tags: [gSchool, reading group]
---

I found this reading to be really interesting.  I took a class all the way back in my freshman year of high school on basic html, and it was surprising how much looked the same.  The things that have changed are pretty exciting - no more fontface, no more cell padding.  I also didn't realize how much that used to be done purely in html is moving over as a function of CSS.

The reading was pretty basic to me, and there wasn't really anything that was confusing.  There were a few techniques I haven't used before, but everything clicked with me as a concept.  The thing that I hadn't ever used before at all was a form, and it was really neat to see everything that you can do with forms.  I didn't have a chance to putz around too much, but I was really interested in trying to build a multiple select box form, so that users are able to select multiple values from a list.  To me, this seemed the most challenging of the forms to implement while the others were pretty straight forward, and is a great way to allow users to select multiple values in the event you have a long list where individual checkboxes may take up too much room.

So, here's my attempt at coding this in a fieldset:

```html
<html>
  <head>
    <title>Favorite ethnic foods questionnaire</title>
  </head>
  <body>
    <fieldset>
      <legend>Demographic Info</legend>
      <label>Age: <input type="text" name="age" /></label>
      Gender:
      <input type="radio" name="gender" value="female">Female
      <input type="radio" name="gender" value="male">Male
      <br />
      <br />
      <form>
        <p>Household Income:</p>
        <select name="income">
          <option value="tier1">0-$30,000</option>
          <option value="tier2">$30,001-$60,000</option>
          <option value="tier3">$60,001-$100,000</option>
          <option value="tier4">$100,001 and above</option>
        </select>
      </form>
    </fieldset>
    <fieldset>
      <legend>Favorite Ethnic Foods</legend>
      <form>
        <p>What are your top three favorite ethnic foods from the following list?</p>
        <p>(You can select more than one option by holding down control on a PC or command key on a Mac while selecting different options.)</p>
        <select name="foods" size="5" multiple="multiple">
          <option value="Mexican">Mexican</option>
          <option value="Cuban">Cuban</option>
          <option value="Italian">Italian</option>
          <option value="French">French</option>
          <option value="Greek">Greek</option>
          <option value="German">German</option>
          <option value="Polish">Polish</option>
          <option value="Lebanese">Lebanese</option>
          <option value="Ethiopian">Ethiopian</option>
          <option value="Indian">Indian</option>
          <option value="Japanese">Japanese</option>
          <option value="Chinese">Chinese</option>
          <option value="Thai">Thai</option>
          <option value="Klingon">Klingon (mmmm... gagh)</option>
        </select>
      </form>
    </fieldset>
  </body>
</html>
```

Which comes out looking like this:

<html>
  <head>
    <title>Favorite ethnic foods questionnaire</title>
  </head>
  <body>
    <fieldset>
      <legend>Demographic Info</legend>
      <label>Age: <input type="text" name="age" /></label>
      Gender:
      <input type="radio" name="gender" value="female">Female
      <input type="radio" name="gender" value="male">Male
      <br />
      <br />
      <form>
        <p>Household Income:</p>
        <select name="income">
          <option value="tier1">0-$30,000</option>
          <option value="tier2">$30,001-$60,000</option>
          <option value="tier3">$60,001-$100,000</option>
          <option value="tier4">$100,001 and above</option>
        </select>
      </form>
    </fieldset>
    <fieldset>
      <legend>Favorite Ethnic Foods</legend>
      <form>
        <p>What are your top three favorite ethnic foods from the following list?</p>
        <p>(You can select more than one option by holding down control on a PC or command key on a Mac while selecting different options.)</p>
        <select name="foods" size="5" multiple="multiple">
          <option value="Mexican">Mexican</option>
          <option value="Cuban">Cuban</option>
          <option value="Italian">Italian</option>
          <option value="French">French</option>
          <option value="Greek">Greek</option>
          <option value="German">German</option>
          <option value="Polish">Polish</option>
          <option value="Lebanese">Lebanese</option>
          <option value="Ethiopian">Ethiopian</option>
          <option value="Indian">Indian</option>
          <option value="Japanese">Japanese</option>
          <option value="Chinese">Chinese</option>
          <option value="Thai">Thai</option>
          <option value="Klingon">Klingon (mmmm... gagh)</option>
        </select>
      </form>
    </fieldset>
  </body>
</html>

