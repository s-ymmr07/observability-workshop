---
title: 2. Synthetics Test Detail
weight: 2
---

1. Deep dive into a   must be successful and long run duration
2. Walk through, screenshots, video and highlight Synthetic vs RUM Web Vitals, Business Transactions, Waterfall, etc.
3. 5 steps/business trans
4. We know there is an issue placing orders, so click on place Order
5. Find POST checkout and click APM link

Right now we are looking at the result of a single Synthetic Browser Test. This test is split up in multiple Synthetic transactions, think of this of a group of one or more logically related interactions that represent a business-critical user flow.

![waterfall](../images/synth-waterfall.png)

1. **Filmstrip:** Offers a set of screenshots of site performance so that you can see how the page responds in real time.
2. **Video:** This lets you see exactly what a user trying to load your site from the location and device of a particular test run would experience.
3. **Browser test metrics:**  A View that offers you a picture of website performance.
4. **Synthetic transactions:**  List of the Synthetic transactions that made up the interaction with the site
5. **Waterfall chart**  The waterfall chart is a visual representation of the interaction between the test runner and the site being tested.

{{% notice title="Exercise" style="green" icon="running" %}}

Similar to RUM, we provide the users ofSplunk Synthetic the option to view the interaction with the Website.
The first part is the film strip, it contains screenshots that where made during the running of the test.

* Change the duration above the film strip from *Every 1s* to *Every 100ms*. This will rebuild the filmstrip with more detail. Notice that building the initial web page increased from 2 screenshots to 20. This will help you see fine grained interactions when required. (**Tip** click on the film strip and use your left and right arrow to move between screen shots)
* In the Video pane, press on on Play **▶** and see the test being run. (Note that you can view it full screen, and if you click the ellipses **⋮** you can change the *playback speed*, view it *Picture in Picture* and even *Download* the video.)
* In the Synthetic Transaction pane, click on the first transaction **Home**
* The water fall below will show the list of interactions that are part of this Synthetic Transaction
* In the waterfall find the line ***GET** splunk-otel-web.js*.
* Click on the **>** button on front of it to drop open the MetaData section to see the URL & Request/Response Header information that are part of this specific step in the test. (Useful for debugging issues)
* In the Synthetic Transaction pane, click on the second transaction **Shop**
Note that the filmstrip adjust and moves to the beginning  of the new Transaction.
* Repeat this for all the other Transactions, then select the **Place Order** transaction.

  {{% /notice %}}
