---
layout: post
title: "How Red Cross Uses Data During Global Disasters"
date: 2018-03-21
description: "Dan Joseph gives us an insight into using street-level imagery in disaster response and the challenges they face when time is critical."
image: /img/posts/20180321-canaan.jpg
caption: View from a Red Cross vehicle mapping in Haiti
author: Dan Joseph
tags:
  - Mapillary
---

_<span class="cross-post">This was originally posted on the [Mapillary Blog](https://blog.mapillary.com/update/2018/03/21/how-red-cross-uses-data-during-global-disasters.html).</span>_

As the world’s largest humanitarian network, Red Cross and Red Crescent teams are present in nearly 200 countries. I’m on a small team of geo-nerds at the [American Red Cross](http://www.redcross.org/about-us/our-work/international-services) focused on international disaster response, resilience, and recovery. We help create, store, and use data to increase the efficiency and impact of our humanitarian mission.

In the immediate aftermath of disasters, it’s amazing to work with Red Cross volunteers who may have lost everything but still show up to help others. And it’s exciting to use technology to support the resilience and power of humanity.

In my role, I’m always trying to figure out better ways to gather facts and figures, bits of data; then process, organize, interpret, and present the data so that it becomes actionable information. For example, the number of damaged houses in a single municipality does not help in understanding the overall situation. But that number can be aggregated with the damages reported in all the other municipalities, and combined with population data in order to calculate the percentage of damaged houses, which can then be visualized using an information product such as a choropleth map.

![map of damages across municipalities in the Philippines after typhoon Hagupit/Ruby](/img/posts/20180321-damage-map.jpg)
<span class="post-caption">Visualizing the extent of damage across municipalities in the Philippines after typhoon Hagupit/Ruby</span>

My team provides information to a variety of audiences with different needs. Sector specialists—for example water and sanitation or shelter leads—benefit from knowing what data is available, what data their teams should collect, and information products that help them assess a situation and analyze response options at a granular level. People leading the entire disaster response need insight into the plans and progress of all the different sector components, as well as awareness of how the pieces relate to the larger disaster situation.

Headquarters staff require a big-picture overview to place individual disasters in a global context. Good information management requires linking those needs, streamlining data collection and analysis, and effectively transforming and disseminating results. It helps to be creative in the use of secondary data sources, primary data collection, and analysis tools.

Spreadsheet software and structured tables are at the core of our toolkit but we are always on the lookout for new tools and sources of data. We love OpenStreetMap (OSM). Understanding places and the "where?" of things is vitally important in disaster response. Not just for getting from point A to point B but for coordination, understanding needs, tracking impact, identifying gaps, and a multitude of other concerns. OSM lets us engage both digital volunteers and local communities through initiatives like the [Missing Maps](https://www.missingmaps.org/) project, to improve the availability, detail, and accuracy of geographic data.

![Red Cross volunteers in South Africa and Bangladesh mapping their communities](/img/posts/20180321-community-mappers.jpg)
<span class="post-caption">Left: volunteers with the South African Red Cross Society map their communities in Khayelitsha, Cape Town as part of a [fire sensor project](http://www.missingmaps.org/blog/2015/09/15/fire-sensor/) <br> Right: volunteers with the Bangladesh Red Crescent Society use Field Papers and OpenMapKit to add detail to OSM in Dhaka</span>


## How we’ve used Mapillary

There are limits to what we can interpret and extract from satellite imagery. Mapillary provides an exciting way to gather images from a different perspective and we’ve collected imagery in a variety of contexts.

The landscape in Haiti is still in flux and continuously changing eight years after a devastating earthquake. The hills north of Port-au-Prince were settled in the aftermath of the earthquake and are now home to more than 200,000 people. The American Red Cross has been supporting residents through health, infrastructure, and livelihoods programs. We’ve worked with the Haitian Red Cross to improve Mapillary coverage in Canaan to help document the rapidly urbanizing area.

<iframe width="600" height="450" src="https://embed-v1.mapillary.com/embed?version=1&filter=%5B%22all%22%5D&map_filter=%5B%22all%22%5D&map_style=Mapbox light&image_key=VK930eto4fz8sxOFb7zZ8w&x=0.5&y=0.5&client_id=S1FUamFnYXBpN2NDSWplbDRtRUJoUToyZjIyYjEyMjJkNTU4ZWZj&style=classic" frameborder="0"></iframe>

In Dominica after the devastation wrought by hurricane Irma, as Red Cross teams travelled around the island assessing and providing support, they also gathered Mapillary imagery to help document the aftermath. The images provided a powerful glimpse into the challenges faced by communities impacted by the storm, situational awareness for organizations responding to the disaster, and created a baseline which could be used to examine changes during the recovery process.

The Philippines is frequently in the path of major storms. Typhoon Haiyan, the strongest storm ever recorded in the country, struck in 2013. Thanks to the generosity of donors, the American Red Cross has been able to work alongside the Philippine Red Cross on [recovery activities](http://www.redcross.org/about-us/our-work/international-services/haiyan-recovery) that include training volunteers in communities on disaster prevention and preparedness.

As part of the work, we were able to improve Mapillary [coverage](https://www.mapillary.com/map/im/Qv38Gt47pSndHmJm9zje6Q) and additionally collect aerial imagery with drones. [Cross referencing](https://americanredcross.github.io/ttl-imagery/) between these different images allows communities to build a more complete picture of their towns. Up-to-date OSM data derived from the images can be used to create accurate maps, which are valuable for planning and as tools for responding to any future disasters.

## Thinking about the future

Most of our use of Mapillary to date has been to capture a snapshot in time or to facilitate OSM mapping. What else could the platform be used for?

Understanding road conditions in the aftermath of a disaster can be vital to operations. It helps answer questions about concerns such as the types of vehicles that can be used to transport relief supplies to an affected community.

In Dominica, MapAction was producing a [physical action constraints](https://maps.mapaction.org/dataset/dominica-access-constraints-v7) map from narrative comments collected piecemeal from various people. If initial assessment teams efficiently collected street level imagery, combined with some sort of tagging analysis, it could more comprehensively reveal access constraints and greatly facilitate logistics planning. Logistics specialists working in the response could check roads to estimate what size of trucks might be used without having to personally travel every route.

The status of local markets can guide decisions about the methods for providing support to a disaster-affected population. If shops and financial institutions like banks are able to reopen quickly, giving cash to affected people may be a better option than shipping in relief supplies to distribute; it provides the dignity of choice and follow-on boosts to the local economy. Could market assessments, comparisons, and tracking over time be facilitated by street-level 360 images?

Mapillary already has the ["time travel"](https://help.mapillary.com/hc/en-us/articles/115001778685) feature to compare images from two different times. Understanding how places have changed is important in the aftermath of a disaster and throughout communities’ recovery. Could analysis of change be automated and extended beyond an image slider? What if sign detection or 3D point clouds of an area could be analyzed to efficiently identify infrastructure that has been destroyed in an earthquake or typhoon?

<iframe width="600" height="450" src="https://embed-v1.mapillary.com/embed?version=1&filter=%5B%22all%22%5D&map_filter=%5B%22all%22%5D&map_style=Mapbox light&image_key=kfimRCaf4MQzrf_jKvSX8Q&x=0.5&y=0.5&client_id=S1FUamFnYXBpN2NDSWplbDRtRUJoUToyZjIyYjEyMjJkNTU4ZWZj&style=classic" frameborder="0"></iframe>
<span class="post-caption">Post-disaster imagery from Dominica: like in a lot of places, there is no pre-disaster imagery available</span>

There tend to be bottlenecks in our Mapillary workflows. Connectivity is a big one. Telecommunications are usually disrupted by disasters. The American Red Cross can deploy VSAT systems for satellite internet but the bandwidth needs to be shared among many users. Uploading thousands of images and then being able to efficiently navigate a web-based viewer can be a challenge. However, we frequently face connectivity challenges, so have no doubt that such issues can be overcome.

American Red Cross uses [Portable OpenStreetMap (POSM)](https://github.com/posm) to bundle tools and data for mapping work onto a small, portable server that can be used in completely disconnected environments. Could some sort of Mapillary-lite be developed and included in the POSM stack? POSM can already host tiles for a locally stored basemap. What if it also had a simplified way to geo-locate and view sequences locally?

Could there be a Mapillary service to facilitate tiered uploads? For example, quickly upload low-resolution copies of images and then replace them later with higher resolution ones once connectivity has improved and urgency for data has subsided. Or perhaps, the upload of the high-resolution copies could be prioritized based on remote requests. Images tagged through crowd-sourced campaigns as high-interest could be prioritized, such as those of a damaged bridge over images of a straight highway.

In the days immediately following a disaster, every hour counts and the value of data can decrease quickly. The idea is that people outside the disaster zone would benefit more from quickly having access to a large number of lower-resolution pictures instead of a slow trickle of full-resolution pictures, although you would eventually want the high-resolution images in the main database.

It is exciting to track improvements to algorithms, cameras, and tools. We hope to see even more ways to collect and use Mapillary street-level imagery. I’d love to know your ideas, what’s worked, the issues you’ve faced, and the upcoming developments you’re most excited about!

_You can follow Dan ([@danbjoseph](https://twitter.com/danbjoseph)) and the American Red Cross ([@RedCross](https://twitter.com/RedCross)) via Twitter._

![Dan setting up a camera on the car hood for mapping](/img/posts/20180321-camera-setting.jpg)
<span class="post-caption">Dan setting up a camera on the car hood for mapping</span>

