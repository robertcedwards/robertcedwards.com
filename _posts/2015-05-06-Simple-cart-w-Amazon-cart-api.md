---
layout: post
title:  "Simple Cart JS with Amazon Cart API"
date:   2015-05-06
---
The beginnings of building a Simple Cart powered Amazon cart using Add to Cart API




```
<form method="GET" action="http://www.amazon.com/gp/aws/cart/add.html">
  <input type="hidden" name="AssociateTag" value="storeid-20"/>
  <input type="hidden" name="SubscriptionId" value="[AWSAccessKeyId]"/>
  <input type="hidden" name="ASIN.1" value="B00003CWT6"/><br/>
  <input type="hidden" name="Quantity.1" value="1"/><br/>
  <input type="image" name="add" value="Buy from Amazon.com" border="0" alt="Buy from Amazon.com" src="http://images.amazon.com/images/G/01/associates/add-to-cart.gif">
</form> 
