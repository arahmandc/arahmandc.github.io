---
layout: post
title: "POSM 0.8 - Big changes"
date: 2018-09-24
description: 
image: /img/posts/20180924-skullcanyon.jpg
caption: An Intel NUC running POSM
author: [Dan Joseph, Seth Fitzsimmons]
tags:
  - POSM
---

_<span class="cross-post">This was originally posted on the [Missing Maps Blog](http://www.missingmaps.org/blog/2018/09/24/posm-release/).</span>_

## POSM

POSM was created to integrate best-of-breed tools from a variety of sources and developers on a single device that can be deployed to the field alongside Red Cross staff and volunteers and facilitate mapping efforts, particularly when internet access is absent. Initially conceived primarily for OpenStreetMap data collection, we’ve had fun pushing the limits of POSM in a variety of situations. Plus, it’s been exciting to see various groups take in interest in the software, some for use cases we never considered! We’ve just released a new version of POSM with many exciting changes.

## Big changes

POSM was first released in early 2016 and ran on Ubuntu 14.04, which was the Long-Term Support release at the time. POSM now runs on Ubuntu 18.04 LTS, which means a more robust and modern operating system as well as support through 2023 instead of April 2019. The versions of Node.js and Ruby included have also been updated to 8.11 and 2.4 respectively, extending their support windows. 

The POSM install now includes [OpenMapKitServer v0.12.0](https://github.com/posm/OpenMapKitServer) which brings in a lot of the great changes by [Wille Marcel](https://twitter.com/_wille) and [Humanitarian OpenStreetMap Team (HOT)](https://www.hotosm.org/). OMK Server has a new, more user-friendly GUI that makes it easier to manage forms and browse submissions.

POSM OpenDroneMap API has been replaced with [WebODM](https://www.opendronemap.org/webodm/). WebODM and the POSM OpenDroneMap API were started at around the same time; WebODM’s ambitions have always been much larger, but it wasn’t ready to be incorporated when we first included drone imagery processing capabilities. We’re very happy to be able to include it now. In addition to providing a GUI for OpenDroneMap, it incorporates the POSM GCPi tool for working with ground control points, a more flexible viewer for ortho images and digital surface models, as well as a 3D viewer for generated point clouds. By bringing OpenDroneMap directly into POSM via WebODM, it should be much easier to update the image processing powers of POSM as those projects continue to improve.

There are now multiple flavors of installer. Incorporating OpenDroneMap into the base POSM installer image dramatically increased its size, so we’ve created multiple variants to limit download size when drone imagery processing is unnecessary. For OpenDroneMap functionality you’ll want the SuperPOSM and POSM AUX variants. POSM AUX can be used to run WebODM across multiple NUCs, controlled by a single SuperPOSM instance. POSM AUX is a stripped down version of POSM that only runs [node-OpenDroneMap](https://github.com/OpenDroneMap/node-OpenDroneMap) and automatically registers worker nodes when one or more POSM AUX instances are present on the same network as a SuperPOSM.

Also worth noting is that the install process should be more reliable, and there have been various bug fixes and UI/UX improvements to each of the various components. For example, the POSM Admin UI is now mobile-friendly and can be configured to only show components that have been installed. It’s a little thing, but Windows 10 on certain laptops is more able to connect wirelessly than before.

Everything is open. You can check out all the details of the updates over on GitHub and grab the latest [release](https://github.com/posm/posm-build/releases). 

## The future

POSM documentation has gotten rather fragmented, with notes and guidance scattered across different readmes and websites.  We’re working on consolidating and updating all documentation and plan on releasing an updated site with all documentation soon.

The new documentation will include the process used to add WebODM into POSM. Having those steps available as a guide should make it easier to add other modules, following the example of WebODM.

POSM started as a mapping stack, and we’d like to see it’s functionality continue to expand in that area as well as expand into new areas. We think there are opportunities to incorporate street-level imagery collection and analysis. There’s a [guest post on the Mapillary blog](https://blog.mapillary.com/update/2018/03/21/how-red-cross-uses-data-during-global-disasters.html) about how Red Cross wants to use such data during disasters 

The POSM AUX variant let users set up a passel of POSMs to manage multiple different processing tasks through a single user interface. We’re hoping someone contributes or funds changes to the OpenDroneMap project so that WebODM can further be used to distribute a single large processing task across multiple nodes. OpenDroneMap contributors have already done some initial work related to this challenge.

There’s a lot going on with our favorite mobile data collection software suite, OpenDataKit (ODK). There’s the ODK2 tools as well as changes in the ODK1 ecosystem like the release of ODK Central, a new server option. What could be combined into the POSM stack to help meet user needs?

In the world of hardware, Amazon has come out with their AWS Snowball device. It could represent a deployment option for POSM. Humanitarian OpenStreetMap Team has already [taken a look at the new technology](https://www.hotosm.org/updates/new-technology-for-aerial-imagery-in-disaster-response/).

## Conclusion

As always, we welcome feedback, [logged issues](https://github.com/posm/posm/issues), bug reports, feature requests, or better yet pull requests etc. If you’ve used POSM for one of your projects, we’d love to hear about it. For any of the above and more, get in touch on the HOTOSM Slack in the #posm channel. You can sign up [here](http://slack.hotosm.org/).