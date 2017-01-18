---
layout: post
title: Benson, MTA Subway Traffic Analysis
---

Week 1 at Metis is up and running. Our group worked out a somewhat clean MTA Turnstile dataset for our first project, Benson. We analyzed and recommended the best stations for street recruitment and mapped income by subway station. Now that we've presented, the results of which can be found [here](https://github.com/bauer1331/Metis_Projects/blob/master/Benson6.pdf), in hindsight the errors we overlooked or did not include are glaring. 

We started by looking at the sum of total traffic in a variety of time intervals - date-time, date, and time. We looked by station, we looked at certain stations in high income areas, which gives a good indication of comparable ridership between stations. However, as a client, I would want to know what foot traffic I should expect within a certain four hour window. We could present one week's data and show true sums of each date-time's four hour interval. However, if we wanted to use any more data, such as multiple weeks, we would need to move beyond a sum to know what kind of foot traffic to expect while canvasing on the street at a certain day and time of the week. 

Our group considered this and took the average into account. However, we took the average of entries and exits over each four hour period. On its face, this seems reasonable. What it is doing without intermediate processing is taking the average of each turnstile for each station, not the average of ridership for any particular station. 

For example, York St. is our number one traffic station for all stations in high income areas. York St. also only has one entry and exit, which means that a smaller number of turnstiles take in all the traffic, where stations usually have multiple entries and exits. Comparing York St. and a station with the exact same total traffic but two entries would have very different averages when taken straight from the turnstile data, where York St. would show higher traffic on average. 

Instead what we needed to do was, first sum the turnstiles together for each station and each date-time four hour period. Only then can we take the average for any particular time of day or the average for any day to understand traffic for a particular station. 



