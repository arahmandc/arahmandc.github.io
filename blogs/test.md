---
layout: post
title: "POSM 0.9 - Passel of POSMs"
date: 2019-08-07
description: 
image: /img/posts/20190903-passel.jpg
caption: Testing distributed processing across multiple Intel NUCs
author: [Dan Joseph, Seth Fitzsimmons]
tags:
  - POSM
  - OpenDroneMap
---

OpenDroneMap (ODM) is an open ecosystem of solutions for collecting, processing, analyzing and displaying aerial data. American Red Cross has used it when conducting drone mapping and trainings with the Philippines Red Cross, Haitian Red Cross, and Belize Red Cross. We’re excited to have been able to fund some recent improvements that create exciting opportunities when running ODM with POSM, while also benefiting the overall ODM project. The changes to ODM included: extension and modifications to ODM's split-merge code to support local and distributed workflows, and changes to the NodeODM API/proxy. What this means for you, is that it’s now possible to process large datasets on a cluster of machines faster by distributing the dataset over multiple nodes.

The newest POSM release brings in the ODM updates and lets you distribute the processing of large image sets across a passel of POSMs. We were ready to make the release available; however, please note that we are still running some tests and updating [documentation](http://posm.io/docs/posm/passel/). You can expect more guidance on the new functionality and at least one minor POSM release in the near future.

Why invest in open source? American Red Cross could have purchased many years of licenses for proprietary photogrammetry software instead of supporting ODM. 

* Commercially available products often aren’t created with a primary focus on humanitarian use-cases. Because ODM is open source we can easily include it on POSM and better integrate it into our humanitarian workflows. Building on an open source foundation means we can spend less money and time building, and have more resources for learning and doing.
* The maintainers of ODM have done significant amounts of unpaid work improving tools that are available for free and helping people leverage the technology. The tools and accompanying support has helped us on our drone mapping journey. It has also benefited other organizations and individuals and helps to level the innovation field, making it easier for a more diverse group to improve their programs with new technologies. Our investment supports the developers and enables them to spend focused time on improving ODM.
* This American Red Cross investment makes the tools better for everyone, not just license holders. A ripple effect means our humanitarian colleagues already mapping with drones in the Belize Red Cross and Indonesian Red Cross benefit, as well as any other Red Cross or Red Crescent National Society that wants to include ODM in a drones for mapping workflow.

What kind of reduction in processing time is possible? We ran some tests of a 3,927 image dataset - the same dataset visible in the screen grab below - on several different numbers of two different models of Intel NUC. The processing times below are in hours:minutes.

| # of NUCs | NUC6i7KYK  | NUC8i7BEH1  |
|-----------|------------|-------------|
|         1 | `63:12`    | `55:46`     |
|         2 | `36:31`    | `31:08`     |
|         4 | `22:07`    |             |
|         6 | `19:51`    |             |

Notes about the tests:
- We adjusted the following parameters: `min-num-features: 9000, split: 500, split-overlap: 120`. 
- All the NUCs had 32GB RAM and a 500GB solid state hard drive installed. 
- The times are calculated from the first and last timestamps saved to the log file. The first timestamp occurs after images are uploaded and resized, and the last time stamp occurs before postprocessing steps such as the generation of base and overview tiles. We think the actual times are between 1.5 and 2.5 hours longer than those listed above. 
- The [NUC8i7BEH1] currently costs about $80 more than the [NUC6i7KYK] but does provide a performance speed boost.

[NUC6i7KYK]: https://www.intel.com/content/www/us/en/products/boards-kits/nuc/kits/nuc6i7kyk.html
[NUC8i7BEH1]: https://www.intel.com/content/www/us/en/products/boards-kits/nuc/kits/nuc8i7beh.html

![the WebODM interface](/img/posts/20190903-culasi.png)
<br><span class="post-caption">The WebODM interface on a POSM showing a completed processing task</span>

We also continue to make small improvements that resolve bugs users have identified and improve the stability of the platform. See the [v0.9.0](https://github.com/posm/posm-build/releases/tag/v0.9.0) and [v0.9.1 release descriptions](https://github.com/posm/posm-build/releases/tag/v0.9.1) for a complete list of notable changes. 

A big thank you to Piero Toffanin of [Masserano Labs](https://www.masseranolabs.com/), Seth Fitzsimmons ([@mojodna](https://twitter.com/mojodna)), and Stephen Mather ([@smathermather](https://twitter.com/smathermather)) for all their help.

Grab the latest [POSM release](https://github.com/posm/posm-build/releases), check out the [documentation](http://posm.io/docs/), log [issues](https://github.com/posm/posm/issues) on GitHub about any bugs or suggestions, follow [@awesomeposm](https://twitter.com/awesomeposm) on Twitter, and get in touch ([@danbjoseph](https://twitter.com/danbjoseph) / [daniel.joseph@redcross.org](mailto:daniel.joseph@redcross.org)) if you want to chat use-cases or coordinate on making the future of drones in humanitarian action even more exciting!
