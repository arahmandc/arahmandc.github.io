---
layout: post
title: "Supporting Open Data Kit"
date: 2019-01-08
description: 
image: /img/posts/20190108-supporting-odk-phones.jpg
caption: Phones packed and ready for data collection by the Philippine Red Cross
author: [Dan Joseph]
tags:
  - open source
  - Open Data Kit
---

## Open Data Kit and the benefits of open source

The [Open Data Kit](http://opendatakit.org) (ODK) community produces free and open-source software for collecting, managing, and using data in resource-constrained environments. The various ODK tools enable cost effective, scalable, and user-friendly implementation of mobile data activities.

Many of ODK’s users are engaged in humanitarian, environmental, development, and civic work. These users may not be able to afford software that requires purchasing a subscription or license. In ODK, they have a robust and accessible mobile data collection solution that is free and open source. ODK is supported by developers, users, organizations, and others giving what they can, when they can. Members of the community write code, fix bugs, create manuals and documentation, help each other troubleshoot via an online forum, give feedback, suggest changes, fund improvements, and tell others about how great the ODK tools are!

ODK has many advantages due to being an open source project. Different groups are able to pool limited resources and share in the work. The software is not tied to any one organization which helps to mitigate software discontinuation risks. A diversity of voices can suggest feature ideas and help realize an effective evolution of the software. Investments have a ripple effect, with small contributions benefiting a large group of users and stakeholders. 

## Open Data Kit usage in the Global Red Cross Red Crescent Network

One of the key components is ODK Collect, an Android app enabling users to retrieve, fill out, and submit surveys digitally from a smart device. [@OpenDataKit](https://twitter.com/OpenDataKit/status/1110995026916593664) tweeted on March 27, 2019: “In the last year, ODK Collect has had 2,500,000 users! The app now runs on 12,000 different devices, supports 50 languages, and is most used in Southern Asia, East and West Africa. Oh, and in the time it's taken you to read this tweet, 15 forms have been submitted using Collect.”

Staff and volunteers of the Red Cross Red Crescent network are among the 2.5 million users in the past year of ODK Collect and other ODK software like the Aggregate server and the Briefcase desktop app. Conducting damage assessments and registering people for relief distributions are two of the many ways the technology can be used to improve the efficiency and impact of humanitarian action.

![tweets from Namibia Red Cross and Indian Red Cross about using ODK](/img/posts/20190108-supporting-odk-society-tweets.png)
<br><span class="post-caption">Tweets from Namibia Red Cross and Indian Red Cross about using ODK</span>

Paid software is not an equally affordable expense around the Red Cross and Red Crescent network, and benefit only the National Society for which the software is purchased. By using and sharing free and open source software within our global network, the costs of technology adoption are much lower. By investing in commonly used open source such as ODK, it also helps the software work well for everyone. 

Some of the Red Cross and Red Crescent investment is through community involvement. It helps ODK when people blog or post on social media about their positive experiences using the software. It helps when people suggest new features or report bugs in the software. It helps when people answer support questions on the community forum. I serve on the ODK Suite Technical Steering Committee, and Raquel Bernedo from Spanish Red Cross serves on the ODK-X Suite Technical Steering Committee. Community is important, but it’s also financial support that keeps the project running and maintained, helping to quickly implement bug fixes and new features, by funding ODK developers.

## Process

The [American Red Cross](https://www.redcross.org) was able to support improvements to ODK; we selected the improvements out of both ideas solicited from the Red Cross and Red Crescent network and a review of existing items on the project roadmap that lacked funding. We narrowed the ideas based on relevance to humanitarian data collection, past challenges when using ODK, the amount of our funding, and the potential magnitude of the benefits to the wider ODK community.

We chose Nafundi to implement the improvements. Nafundi is a professional services company that invests significant time and energy in developing and maintaining the various ODK components and contributing under the project’s open license so that anyone can use the technology. Nafundi's principals, Yaw Anokwa and Hélène Martin, are lead maintainers on ODK so given their years of work on ODK and long-running support of the project, they made an ideal partner.

Each idea went through an open feedback and consultation phase. Conversations occurred mostly on the community forum, and helped ensure the technical feasibility of the ideas, check our assumptions, and confirm compatibility with the larger ecosystem. Developers then coded the improvements and pushed them out in the next release of the products.

## Contributions

### Export standard geoformats

The American Red Cross funded a data export option that allows the user to get their survey data in a GeoJSON geographic file format instead of the standard spreadsheet. The functionality makes it easier to use the data in a GIS or other downstream tool. The functionality was intended to be implemented in both Aggregate and Briefcase. Briefcase v1.13 included the feature  for both the graphical user interface and via command line. Implementing the feature in Aggregate with Google App Engine support, a key part of many existing server deployments, was going to be too costly so we pivoted that funding into additional features (see the last section below). The community discussion for the feature can be found on the [forum](https://forum.opendatakit.org/t/add-a-geojson-export-to-briefcase-and-aggregate/15184). The improvement was tracked and implemented on [GitHub](https://github.com/opendatakit/roadmap/issues/26) and released in [Briefcase v1.13](https://forum.opendatakit.org/t/odk-briefcase-v1-13/16442). 

![a tweet from @OpenDataKit about the Briefcase release](/img/posts/20190108-supporting-odk-tweet-briefcase.png)
<br><span class="post-caption">A tweet from [@OpenDataKit](https://twitter.com/i/web/status/1066995088511897600) about the Briefcase release</span>

### Collect GPS coordinates for audit purposes

We funded an optional feature to occasionally collect GPS coordinates in the background to provide evidence that data was collected in a particular place. There are many legitimate use-cases for this feature but also the potential for abuse; the community discussion around this feature included a good debate about privacy. The discussion for the feature can be found on the [forum](https://forum.opendatakit.org/t/collect-extend-audit-log-to-include-gps-coordinates/15162). The improvement was released in [Collect v1.20 Beta](https://forum.opendatakit.org/t/odk-collect-v1-20-beta/18021) along with related updates to ODK XForms spec, pyxform, XLSForm Online, XLSForm Offline, and the user [documentation](https://docs.opendatakit.org/form-audit-log/).

![a tweet from @OpenDataKit about the ODK Collect release](/img/posts/20190108-supporting-odk-tweet-odk-audit.png)
<br><span class="post-caption">A tweet from [@OpenDataKit](https://twitter.com/arphp/status/1100019065882583041) about the Collect release</span>

### Standardize on ISO8601 when exporting `dateTime` from Aggregate and Briefcase

Our team funded standardization of date and time formats in data exports. Dealing with dates, times, and time zones in software can get really complicated. There are many different ways various devices record time and we needed to support a standard date format to make data analysis easier. The community discussion for this feature can be found on the [forum](https://forum.opendatakit.org/t/standardize-on-iso8601-for-date-and-time-exports-in-briefcase-aggregate-central/15159). Aggregate v2.0 exports dates in the very popular ISO8601 format. Briefcase will also export standardized dates, but since it is a potentially breaking change for users it is being held for Briefcase v2.0 and is tracked on [GitHub](https://github.com/opendatakit/briefcase/issues/720).

### Additional features

Due to necessary changes in the implementation of some of the originally envisioned features, and some of the work taking less time than predicted, we were able to fund a couple more features.

In Briefcase it is now easier to create an audit file with data from all submissions, it’s possible to remove group names from CSV header (making data analysis easier), and some of the underlying software processes were improved.

Aggregate was improved to have more consistent date and location formats within the user interface, and the code cleaned up to reduce the size of the application from 146 MB to 35 MB.

## Everyone can contribute

The American Red Cross plans to continue to find ways to support ODK in the future. We hope you might consider doing so as well. You can fund bug fixes and maintenance, fund improvements, contribute to the conversations on the forum, or just spread the word. Get started by heading over to the ODK forum to say hi and [introduce yourself](https://forum.opendatakit.org/t/introduce-yourself-here/6671)!