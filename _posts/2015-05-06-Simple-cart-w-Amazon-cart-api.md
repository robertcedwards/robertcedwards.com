---
layout: post
title:  "Simple Cart JS with Amazon Cart API"
date:   2015-05-06
---
The beginnings of building a Simple Cart powered Amazon cart using Add to Cart API

The general idea is to add items from the site to a cart. Those items are found on Amazon but are listed here in a nice interface with search and filtering. The items are then add to an Amazon cart and the user is directed to confirm those product being added to the cart on Amazon.
For our first attempt we used Simplecart JS, but moving forward a custom Angular based solution will be used to handle the cart plus the search and filtering.

<hr/>
Update:
I found a few node.js libraries that use the Amazon AWS Product API.
I was also able to find an example of a simple Angular.js cart to use for my purposes.

https://affiliate-program.amazon.com/gp/associates/help/t1/a10
https://affiliate-program.amazon.com/gp/advertising/api/detail/main.html
http://mrbool.com/angularjs-creating-a-shopping-cart-application/32183
https://github.com/Stamplay/stamplay-foodme
https://jsfiddle.net/robertcedwards/kfh5swdj/4/


```
<form method="GET" action="http://www.amazon.com/gp/aws/cart/add.html">
  <input type="hidden" name="AssociateTag" value="storeid-20"/>
  <input type="hidden" name="SubscriptionId" value="[AWSAccessKeyId]"/>
  <input type="hidden" name="ASIN.1" value="B00003CWT6"/><br/>
  <input type="hidden" name="Quantity.1" value="1"/><br/>
  <input type="image" name="add" value="Buy from Amazon.com" border="0" alt="Buy from Amazon.com" src="http://images.amazon.com/images/G/01/associates/add-to-cart.gif">
</form> 