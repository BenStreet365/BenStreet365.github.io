---
layout: post
title:  "Dynamic Groups VS 'All Devices'/'All Users'... and filters!"
tags: intune filters devices groups
category: Microsoft Intune
permalink: /dynamic-groups-vs-all-devices-all-users
---

# Dynamic Groups VS 'All Devices'/'All Users'... and filters!

You may not know this, but a group containing All Devices and Intune's built in 'All Devices' group both behave differently. To save some time, I'm going to abbreviate 'All Devices'/'All Users' to ADAU.

If you create a group, manually add in all of your devices or using a dynamic rule, there is a performance difference between the two. The group is stored within Microsoft's Entra system, which **is** seperate to Intune. The built-in ADAU option is built directly into Intune which works quicker than relying on the Entra sync.

Now your first thought when hearing this information is likely exactly what mine was.

- "That's great and all, but I *don't want to deploy to all devices*."

The great news here is that this is where Filters can come to save the day. Personally, I try to use ADAU and filters wherever I can. It helps when you need to deploy certain profiles or apps to certain models and helps lower the amount of groups flooding your already busy Entra system.

Future ref: https://learn.microsoft.com/en-us/mem/intune/fundamentals/filters