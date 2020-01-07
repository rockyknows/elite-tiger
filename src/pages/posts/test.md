---
template: post
title: Defender ATP Setup
subtitle: " this was quite an accomplishment and we're only half way to our goal:
  Defender ATP into Intune!"
date: 2019-12-12T06:00:00.000+00:00
thumb_img_path: "/images/fig1-Windows-Defender-ATP.png"
content_img_path: "/images/743165-636723471701735787-16x9.jpg"
excerpt: 'Personally, this is monumental to my career. '
hide_header: false
defender: []
Topics: []

---
**Defender ATP Setup: High-Level Overview**

I'd like to take this opportunity to especially thank everyone that made this happen, you all know who you are! (will most likely post a team photo). Personally, this is monumental to my career. I've done other projects for this company but wow, this was quite an accomplishment and we're only half way to our goal: Defender ATP into Intune!

Most likely this will be an on-going post that I will need to keep working on the weekends.

So here's the last 30 days so far: ![](/images/Annotation 2020-01-07 082123.png)

A month ago, we started with Ring 0 (My co-workers and I) with removing McAfee using their official removal tool. And we've downloaded the SCCM 2012 onboarding package from the ATP settings. 

![](/images/Annotation 2020-01-07 082408.png)

I can go into more details on a later post, but we've got that sorted out. Now, the policy. I initially wanted SCCM to take all the heavy lifting and I thought its a lot better than deploying the policy (firewall settings, and defender client settings) but that didn't go as plan. Our SCCM back-end team was out for  a whole month. We could not wait until then. 

Therefore, we've gone backwards and pushed the policy via Group Policy. We scoped it to a 'few' security groups to narrow our target. We also scoped it to only apply if it is "Windows 10".  We do have a few Windows 7 and 8.1 but that was too much to handle. They all will be upgraded to windows 10 by the end of the year, so it isn't a big deal. 

Once we got the policy in-place (which took about 10-15 meetings with our security teams), we finally settled with having a full scan weekly schedule to get rid of our mandatory full scan on the McAfee set of rules. That was a bad idea. I'll write another post on that. 

So we got:

1. Onboarding Configuration Policy
2. GPO for Defender Policy
3. McAfee Removal Tool packaged and ready to be deployed

We are now set with making history! We know the policy hits every 75-90mins, so we've settled with deploying it first, and then a few minutes later, the Onboarding and then McAfee Removal. 

**The Results**

The main goal was to remove McAfee Removal, place Defender ATP as the main AV. This goal was simply the most biggest asked I've ever done. For about 3 months, my team and I have prepped for this project but the reality is: You cannot be complacent and not think two to three steps ahead.   
I'm so proud of my team to stick to it during the holidays (Thanksgiving and December Holidays). 

Thirty Days from the official deployment, we are now sitting around 7.2k devices mostly cloud desktops, and starting to rollout to all physical devices. 

Follow me on twitter [https://twitter.com/atRockyP](https://twitter.com/atRockyP "https://twitter.com/atRockyP") 

***

___

END