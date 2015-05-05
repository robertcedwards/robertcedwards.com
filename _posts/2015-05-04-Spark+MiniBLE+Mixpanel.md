---
layout: post
title:  "Spark + MiniBLE + Mixpanel = Physical Analytics"
date:   2015-05-04
---

http://community.spark.io/t/spark-mini-ble-mixpanel-physical-analytics/11522?u=robertcedwards

I've just finished building out a v1 of an idea I've been working on.
The general idea is to use BLE mini in central mode to detect the UUID of nearby beacons, publish those to the Spark Cloud as a Spark.variable. A node.js script is running using [sparknode][1] & [mixpanel][2] to check for new UUIDs and publish those to Mixpanel as a custom action. I've also include a little logic if a known UUID is found, publish to Mixpanel with a friendly name.
This example requires this separate node script but using base64 we can encode a simple http post using just the Spark. If anyone would like to help me, [nudge nudge][3], that would be awesome.

I've included my Node app and sketch file here:
https://github.com/robertcedwards/SparkyBLE-Mixpanel

Original sketch came from:
[Detect iBeacons using Spark Core and BLE Mini][4]
 :+1: (thanks to @krvarma for his great work)

  [1]: https://www.npmjs.com/package/sparknode
  [2]: https://www.npmjs.com/package/mixpanel
  [3]: https://mixpanel.com/help/reference/http
  [4]: https://community.spark.io/t/detect-ibeacons-using-spark-core-and-ble-mini/5554


```node npm install``` in the root directory to install Mixpanel and Sparknode dependencies.
Enter your Spark Account Token and Device ID along with your Mixpanel account token in config.json
Run the app with ```node app.js```

Procfile included to run with Heroku
