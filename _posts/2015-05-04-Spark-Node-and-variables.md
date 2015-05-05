---
layout: post
title:  "Passing Variables from Spark Cloud to Node.js"
date:   2015-05-04
---

We have an app running on Heroku that acts as the Spark to SMS gateway.
Originally we had the values for sending text messages hardcored in the Heroku app.
We need to be able to changes the message that is being sent via a admin page.
By using an interface that requires

https://github.com/suda/spark-web-interface
