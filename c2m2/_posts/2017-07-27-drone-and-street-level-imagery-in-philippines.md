---
layout: post
title: "Detailed drone and street-level imagery for mapping in the Philippines"
date: 2017-07-27
description: "In May 2017, the American Red Cross and Philippine Red Cross collected detailed aerial and street-level imagery of areas that have been part of a 3-year Typhoon Haiyan (Yolanda) recovery program."
image: /img/posts/20170727_banner.jpg
caption: Aerial view of one of the barangays mapped by drone
author: Dan Joseph
tags:
  - drones
  - Mapillary
---

_<span class="cross-post">This was originally posted on the [Missing Maps Blog](http://www.missingmaps.org/blog/2017/07/27/drone-and-street-level-imagery-in-philippines/).</span>_

## Tindog Tabang Leyteño (Stand Up, Help Leyteños)

As part of the response to the disaster caused by Typhoon Haiyan (Yolanda), the strongest typhoon ever to make landfall in the Philippines, the [Philippine Red Cross](http://www.redcross.org.ph/) in partnership with [American Red Cross](http://www.redcross.org/about-us/our-work/international-services) implemented Tindog Tabang Leyteño, a 3-year recovery project. The project covers 4 municipalities and 23 barangays. The main goal of the project is to contribute to building safe and resilient communities by identifying and addressing various factors that will help people sustainably rebuild their lives, livelihoods, and assets while ensuring that future climate, environmental, and disaster risks are addressed or minimized.


## Aerial imagery collection

**Background**

Unmanned Aerial Vehicles (UAVs), also known as Remotely Piloted Aircraft Systems (RPAS) or drones, are increasingly used for [humanitarian purposes](http://drones.fsd.ch/en/drones-in-humanitarian-action/). In May 2017, we leveraged drones for comprehensive aerial imagery collection to support the recovery program. High-resolution aerial imagery is a valuable resource when creating value-add information products for response, planning, monitoring, and resilience building activities.

<img src="/img/posts/20170727_compare.jpg" alt="satellite vs drone imagery">
<br><span class="post-caption">Resolution comparison between satellite imagery available on Google Maps (left) compared to drone imagery</span>


**Coordination and legal aspects**

When flying drones, it is important to comply with regulations, conduct activities professionally, and operate safely. Failing to do so could result in backlash against the future utilization of the technology. An FAA certified remote pilot from the American Red Cross GIS team as well as a volunteer that is certified were present for the project activities. During planning stages, we talked through the activities with the Philippine Red Cross. Then we communicated with all the local authorities to obtain their approvals. We then obtained all necessary authorizations from the Civil Aviation Authority of the Philippines (CAAP). Preparation for the trip was a several month process!

<img src="/img/posts/20170727_slingshot.jpg" alt="POSM">
<br><span class="post-caption">When flying at 80 meters, kids with slingshots aren't much of a threat but maybe we should have done more information dissemination about our activities! CC-BY Matthew Marek</span>

**Drones**

We took two fixed-wing drones, an [Event 38](https://twitter.com/Event38) E384 and a [Tuffwing](https://twitter.com/TuffWing) UAV Mapper, as well as a small quadcopter, a [DJI](https://twitter.com/djiglobal) Mavic Pro. Due to some technical challenges, and difficulties finding suitably large and clear areas for landing the fixed-wing drones, almost all our mapping ended up being with the Mavic. Because we had two pilots we ended up procuring a second Mavic after the first week to double our coverage speed.

<img src="/img/posts/20170727_mavics.jpg" alt="flying the Mavics">
<br><span class="post-caption">James McDanolds monitors a Mavic in flight while Dan Joseph troubleshoots another, CC-BY Ylla De Ocampo</span>


<iframe width="560" height="315" src="https://www.youtube.com/embed/-nL0WM8rgj4?rel=0" frameborder="0" allowfullscreen></iframe>
<span class="post-caption">Launching the Tuffwing</span>

<img src="/img/posts/20170727_training.jpg" alt="flying the Mavics">
<br><span class="post-caption">James McDanolds teaches Ylla De Ocampo from the Philippine Red Cross how to pilot the Mavic, CC-BY American Red Cross</span>


**Ground control points**

We tested using ground controls points (GCPs) in Barangay Marasbaras. We had 12 large fabric markers with distinct patterns that we placed around the area before collecting imagery. By using handheld Garmin GPS units' waypoint averaging functionality, we could determine more accurate latitude and longitude coordinates for the markers which were then used after image processing to adjust and improve the accuracy of the final map products.

<img src="/img/posts/20170727_gcp2.jpg" alt="ground control point">
<br><span class="post-caption">One of the fabric markers used as a ground control point, CC-BY American Red Cross</span>

<img src="/img/posts/20170727_gcp1.jpg" alt="waypoint averaging">
<br><span class="post-caption">Waypoint averaging with a Garmin GPS unit, CC-BY American Red Cross</span>

<img src="/img/posts/20170727_gcp3.jpg" alt="gcp visible in aerial imagery">
<br><span class="post-caption">One of the GCPs visible in the aerial imagery, CC-BY American Red Cross</span>

## Mapillary

As we travelled between barangays and walked around the areas, we used a variety of cameras to collect street-level imagery. The geotagged images collected with Sony action cameras, 360<sup>o</sup> cameras, and smart-phones were then uploaded to [Mapillary](https://www.mapillary.com/) where they became part of an ever-growing, community built collection of openly licensed street-level images for the world. The images can provide valuable insights; it is possible to observe signage, the condition of buildings, and other aspects of the environment not visible in vertical aerial/satellite imagery. They allow anyone to [#MapillaryExplore](https://twitter.com/mapillary/status/874978591678791681).

<img src="/img/posts/20170727_mapillary.jpg" alt="collecting mapillary">
<br><span class="post-caption">Hiding from the sun while <a href="https://www.mapillary.com/app/?lat=10.859070004872933&lng=124.98645779947196&z=17&pKey=61GREpTo2sVH4BfhTSZm6A&focus=photo&x=0.3017540420440399&y=0.6072076945566833&zoom=0" target="\_blank">collecting images</a> with a 360<sup>o</sup> camera mounted on a pole</span>

## Processing

To process aerial drone imagery, we use an open-source toolkit called [OpenDroneMap (ODM)](https://github.com/OpenDroneMap/ODM#odm). ODM can combine the series of images captured during flight(s) over an area of interest into a single georeferenced image file that can be used for GIS purposes. We can perform this process in offline environments, having incorporated ODM into the set of software tools that we can run on a [POSM](https://github.com/posm/posm#posm) portable server. POSM runs on a small piece of hardware that is plugged into a power source and broadcasts a local wifi signal in order to connect devices. When connected to POSM, users can access several pieces of software, such as ODM and other mapping tools, that are normally cloud-based and require an internet connection.

<img src="/img/posts/20170727_image-folder.jpg" alt="folder of images">
<br><span class="post-caption">A folder full of the individual raw images collected over an area</span>

<img src="/img/posts/20170727_posm.jpg" alt="POSM">
<br><span class="post-caption">Processing imagery on a POSM, CC-BY American Red Cross</span>



## OAM

[OpenAerialMap (OAM)](https://openaerialmap.org/) is a repository of openly licensed imagery and map layer services. We uploaded all the processed imagery to OAM so that it would be easily available for us, and others, to access and use.

<img src="/img/posts/20170727_oam.jpg" alt="OpenAerialMap">
<br><span class="post-caption">Imagery on OpenAerialMap (OAM)</span>

## OpenStreetMap

**OSM in the Philippines**

There is a strong OSM-PH community and OSM is increasingly considered a useful source of geographic data in the Philippines. The Philippines government has recognized the strengths of OSM and its importance in creating “more accurate street-level risk analysis maps for the Philippines. This in turn will be used in improving disaster management before, during, and after emergencies” ([source](https://center.noah.up.edu.ph/map-your-community-in-osm-with-project-noah/)).


**Humanitarian OpenStreetMap Team (HOT) Tasking Manager**

To coordinate the digital volunteers helping to trace the project areas we used the Humanitarian OpenStreetMap Team (HOT) Tasking Manager to divide each barangay up into a grid of tasks to be systematically traced and then validated by a skilled mapper.

**Results**

The drone imagery, and the Mapillary images as well, proved useful for detailed, up-to-date tracing of map features into OSM. The improvements over what was possible using only satellite imagery are striking!

<img src="/img/posts/20170727_palanog-before.jpg" alt="before">
<br><span class="post-caption">Barangay Palanog 37-A before drone imagery was used to update <a href="https://osm.org/go/44Cii0w6h--" target="\_blank">OSM</a></span>

<img src="/img/posts/20170727_palanog-after.jpg" alt="after">
<br><span class="post-caption">Barangay Palanog 37-A after drone imagery was used to update <a href="https://osm.org/go/44Cii0w6h--" target="\_blank">OSM</a></span>

## Next steps
We made all the imagery outputs available through [OAM](https://map.openaerialmap.org/#/125.32379150390624,10.875116370134366,9?_k=xfrwrc) and [Mapillary](https://www.mapillary.com/app/?lat=11.061160979894737&lng=125.00135879610951&z=10).
We've also made the raw datasets of aerial imagery [available](https://docs.google.com/spreadsheets/d/1vX1C0k1TM0op9qQ0m8cXMUsMcUnzw3o7SE5dasOXbf8/edit?usp=sharing) with the intent that they can be used for purposes such as test datasets for the development of tools like ODM. You can check out the imagery in this [web viewer](https://americanredcross.github.io/ttl-imagery/). The outputs will be shared with the communities and local government. The American Red Cross will continue to work with the Philippines Red Cross to utilize the data and think about future use of drones. We will continue to share and progress with our learning, and hopefully fly again soon!

<img src="/img/posts/20170727_kids.jpg" alt="flying the Mavics">
<br><span class="post-caption">Interested kids crowd around to see the screen displaying the status of one of the Mavics as it maps, CC-BY Ylla De Ocampo</span>
