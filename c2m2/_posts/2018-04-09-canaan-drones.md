---
layout: post
title: "Drones over Canaan, Haiti"
date: 2018-04-09
description: Canaan, one of the most populated areas in Haiti, continues to evolve and grow. In December 2017, the American Red Cross covered 35 square kilometers of this area with new drone imagery to assist with population estimates, disaster preparedness programming, and updating OpenStreetMap. 
image: /img/posts/20180409_banner.jpg
caption: Checking the progress of a drone mapping mission, CC-BY Matt Gibb/ American Red Cross
author: [Matthew Gibb, Dan Joseph]
tags:
  - drones
  - Mapillary
---

_<span class="cross-post">This was originally posted on the [Missing Maps Blog](http://www.missingmaps.org/blog/2018/04/09/canaan-drones/).</span>_

## Canaan, Haiti

Eight years after the devastating earthquake in January 2010, the landscape in Haiti is still in flux and continuously changing. For organizations working in Haiti, recovery programs slowly transition to preparedness and disaster risk reduction. More importantly, for over 250,000 people north of Port-au-Prince a patch of land that was once a blank slate transitions into a future. The resourcefulness of this community has been well documented. Since 2014, the American Red Cross has been supporting residents of this community through health, infrastructure, and livelihoods programs.

<iframe width="560" height="315" src="https://www.youtube.com/embed/YopoEuwLf2Y" frameborder="0" allowfullscreen></iframe>

Canaan lies in rolling foothills about 10km north of Port-au-Prince. The population has continuously grown since the earthquake and dense urban areas have developed in central parts. The farther areas are more sparsely populated although this is rapidly changing as can be seen in the amount of ongoing construction. Canaan has grown so rapidly that keeping a map of the area up to date is extremely difficult. Additionally, some communities have become so dense that the satellite imagery commonly used to create maps is not detailed enough to accurately interpret. To address these issues and benefit the communities and other organizations working there, the American Red Cross collected, processed, and made available high resolution, up-to-date, drone imagery for the entire 35 square kilometer area in December 2017.

## Equipment

To collect imagery of Canaan we utilized DJI’s Mavic Pro quadcopter. Flight planning was done with the DroneDeploy app. We could define an area of interest, set a flight altitude, and set desired overlap between images. Higher overlap means the images can be more accurately stitched together but will increase mission time and, later, the processing time as well due to the higher number of images that need to be processed. 

DroneDeploy automatically calculates the number of flights passes over the area of interest and the distance between passes. The app also allows a mission to be resumed after switching out the Mavic's battery for areas that cannot be completed during the approximately 25 minutes of flight time possible on a single battery.

Given the Mavic Pro’s size and sensor capabilities, it took a large number of flights with close together passes. In preparation, we packed 20 batteries and power converters that let us charge batteries in our vehicle while flying.

To improve accuracy of our orthomosaic, at each launch point, ground control points (GCPs) were used. GPS coordinates are taken at the center of the GCP and when the orthomosaic is created, it can be georectified by adjusting the latitude and longitude of the GCP in the image to match those of the collected coordinates.

<img src="/img/posts/20180409_gcp-placed.jpg">
<br><span class="post-caption">Ground control point placed near launch site, CC-BY American Red Cross</span>

Ideally, for an area as large as Canaan we would be able to use a fixed wing drone. We’ve used a platform called the [Tuffwing UAV Mapper](http://www.tuffwing.com/). It has a longer flight time and a camera sensor with a larger field of view allowing for more area to be covered by a single picture. Unfortunately, using the Tuffwing in Canaan was mostly not feasible due to factors like high winds and trouble finding large enough, clear landing areas. We were able to fly the Tuffwing to capture imagery in only one neighborhood.

## Flight Planning

_The best laid plans of mice and men, go oft awry_ - Robert Burns, paraphrased

Failing to plan is planning to fail, so based on what we knew of the Canaan area and the capabilities of the drones we created flight plans and a schedule roughly based on a grid of 1km squares. It was easy to set up what appeared to be a flawless plan from 1,400 miles away; however, perhaps not surprisingly, our plan needed to be adjusted throughout our time in Haiti.

When using drones for humanitarian purposes, an important aspect of the process is community sensitization and buy-in. From other Red Cross work in Canaan there is a fantastic network of community focal points. These community members work with their neighbors and community leaders and facilitate effective communication and cooperation for Red Cross projects in the neighborhood. Red Cross staff worked with the focal points to explain ahead of time the goal of the drone flights and to address any concerns. More information about best practices when using drones in humanitarian contexts can be found on the [UAViators website](https://uavcode.org/).

In some neighborhoods, these conversations were completed faster than others. Because of this, our initial itinerary changed very quickly.

Once we had a better idea of the timeline for which we would be able to fly over certain communities, we worked out a more efficient plan for selecting flight locations. Using our initial grid as guidance, we used an ASTER DEM to identify centrally located high points in the landscape. Using these points, we calculated Voronoi Polygons to have a better idea of reachable areas from a given launch point. We would then edit these polygons to create more "reasonable" (totally subjective) areas for a given flight. We didn't want too many very small areas, as travel time would ultimately take away from flying time. We preferred to send the drone a bit further rather than pack up, travel, and unpack to do a short flight. Ultimately we made judgement calls based on the topography. We created overlap with neighboring flight areas as well as areas between assigned days. The overlap would ensure coverage of a given location in case the direction of the flights varied slightly.

The polygons of the flight areas were converted to `.kml` files and uploaded to the DroneDeploy website. Most flight altitudes were set to 160 meters with 70% side-lap and 80% front-lap. With no UAS regulation in Haiti at the time, almost no air traffic in the area, and very clear lines of sight, we were able to fly at this altitude consistently throughout our mission. After selecting the flight direction (which could be edited upon arrival at the flight location to adjust for wind), the flight plans could then be synced to the DroneDeploy iPad app, which connects to the Mavic Pro flight controller and is used to program the drone for its flight.

## Flying

The pre-identified launch points were converted to `.gpx` waypoints and added to the [OsmAnd](https://osmand.net/) mobile app on our phones.  We could then use the app to navigate to our destinations via the previously traced OSM road network. In most neighborhoods we would travel with the community focal point, and use their knowledge to navigate more efficiently.

Once we were setting up at a launch point, the community focal point would work with us to explain to and demonstrate for onlooking community members, the work that we were doing with the drones.

In addition to flights, we used two Sony Action Cameras to capture street level imagery as we drove throughout Canaan. The imagery of the area can be viewed on [Mapillary](https://www.mapillary.com/app/?lat=18.652149722222248&lng=-72.29545138888886&z=17&pKey=qesHt-3rIoVgYZaYtguNsQ&focus=photo) and [OpenStreetCam](http://openstreetcam.com/details/990741/207). Both forward facing and side facing images were captured.

<img src="/img/posts/20180409_mapillary.jpg">
<br><span class="post-caption">Camera collecting street level imagery for Mapillary and OpenStreetCam, CC-BY American Red Cross</span>

<iframe width="640" height="380" src="https://embed-v1.mapillary.com/embed?version=1&filter=%5B%22all%22%5D&map_filter=%5B%22all%22%5D&map_style=Mapbox light&image_key=qesHt-3rIoVgYZaYtguNsQ&x=0.5&y=0.5&client_id=S1FUamFnYXBpN2NDSWplbDRtRUJoUToyZjIyYjEyMjJkNTU4ZWZj&style=classic" frameborder="0"></iframe>

Over 6 days of flying (with excessive wind grounding us for 2 additional days), we launched and landed the Mavics enough times to collect 28,232 nadir (downward-facing) images. While driving between launch sites we collected 133,109 street level images.

## Processing

At the American Red Cross, we support the development and use of open source software. We are fans of the OpenDroneMap project. Due to the magnitude of images that were collected, we processed the images in 66 separate groups, each less 1000 images, making sure that there was significant overlap of these areas for continuity when later merging them. It took several attempts and and multiple methodologies to identify a process that resulted in a quality orthoimage to be shared. Things that could go wrong, did: hard drives filled up, uploads failed, GDAL installations were messed up, downloads failed, and more. OpenDroneMap has since been improved to better handle such large image sets, so it'll be a lot easier next time!

<img src="/img/posts/20180409_processing.png">
<br><span class="post-caption">Collected imagery and the processing areas, CC-BY American Red Cross</span>

Once the merged orthomosaic was complete, we adjusted the georeferencing of the mosaic using the ground control points that had been laid out at each launch site.

<img src="/img/posts/20180409_gcp-flight.png">
<br><span class="post-caption">Ground control point flag and red marker showing corresponding collected GPS coordinates in an image from the DJI Mavic Pro, CC-BY American Red Cross</span>

The orthomosaic has been added to and can be downloaded from [OpenAerialMap](https://map.openaerialmap.org/#/-72.27829399999999,18.670043999999997,10/user/59ecfc8c31eff4000c3804dd/5ac7d6ca91b5310010e0d4c4?_k=a7m179). New mapping projects have been created on the HOT Tasking manager. Due to the density of the area and presence of existing data, these projects are available to advanced mappers only.

The imagery has been shared with American Red Cross staff as well as partners and organizations working in Canaan to improve population estimates, plan DRR activities, and assist with community planning.
