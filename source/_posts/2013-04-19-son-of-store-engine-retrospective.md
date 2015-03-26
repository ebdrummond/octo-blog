---
layout: post
title: "Son of Store Engine Retrospective"
date: 2013-04-19 15:16 -06:00
comments: true
sharing: true
permalink: /2013/04/son-of-store-engine-retrospective
tags: [son of store engine, gSchool]
---

Son of Store Engine was an interesting project for me.  I started off feeling a little shaky on my Rails knowledge versus Store Engine, and I still feel like I have a ton to learn, but towards the end of the project I felt like the struggle I put in started to pay off.  In the beginning of the project, I began to realize I wasn't ever really sure how my params were being passed back and forth, what the heck was in my session, how I could get information from point A to point B, and by the end, I felt like I understood these things better.  A huge part of this process was the better errors gem and information contained there by default, and in the live shell.  It was enormously helpful to be able to inspect params, what was in my session, and be able to play around in the live shell to manipulate this information to output what I needed.  We had used better errors in Store Engine, but I felt like I didn't know how to harness it's power to my advantage until the latter part of this project.

I also got the chance to put processor controllers and models into play for information that we wanted to render on one page, but involved four different forms and databases.  This was something I attempted to do last project and failed pretty miserably, but I had really wanted to try this project.  It took a little wrangling to get it, but I think the final result was pretty clean code and I'm so glad I know how to do this now.  Here's a snippet:

```
class Checkout

  def initialize(params)
    @guest = Customer.find_by_email(params[:guest][:email])
    @guest ||= Customer.create(params[:guest])
    @shipping = params[:shipping_address]
    @billing = params[:billing_address]
    @credit_card = params[:credit_card]
  end

  def shipping
    new_shipping = ShippingAddress.new(@shipping)
    new_shipping.customer_id = @guest.id
    new_shipping.save
    new_shipping
  end

  def billing
    new_billing = BillingAddress.new(@billing)
    new_billing.customer_id = @guest.id
    new_billing.save
    new_billing
  end

  def credit_card
    new_credit_card = CreditCard.new(@credit_card)
    new_credit_card.customer_id = @guest.id
    new_credit_card.save
    new_credit_card
  end
end
```

Overall, I think our project wasn't great (there's a lot more I would have liked to do with a few extra days), but I think it was pretty good.  The final result is here: [pink-sose.herokuapp.com](http://pink-sose.herokuapp.com/)

It also feels weird to be at the halfway point of gSchool.  It feels like ages ago we were doing logic problems for warmups and getting stressed over Event Manager.  At the same time, it went by quickly with all we've been doing, and I'm hoping that July 19th comes as quickly as well.  My big hope for the second half of the program is that I can manage the stress a little better, and maximize my learning with the time I'm putting in.  I've been putting in about 12 to 14 hours a day during the weekdays on average, and 8 to 12 on weekends when we're working on a project.  At the same time, I feel like there's still so much that we're exposed to that I'm not learning as well as I'd like, and the physical exhaustion and frustration over all the things I haven't been able to pick up yet are taking their toll.
