---
layout: post
tags: purser
date: 2019-08-13
thumbnail: https://user-images.githubusercontent.com/42761785/53145168-2f4e4980-35c5-11e9-867b-8d637671ec23.png
title: "An Update on Purser: The Kubernetes Tool That Saves You Serious Money"
published: true
---

*As posted on [blogs.vmware.com](https://blogs.vmware.com/opensource/2019/08/13/purser-kubernetes-tool-saves-money/) on August 13, 2019*

Just over a year ago, VMware open-sourced Purser, [a Kubernetes extension](https://github.com/vmware/purser) that offers detailed cost insights into cloud native application workloads. In particular, Purser provides visibility into resource use for any specific Kubernetes cluster, including real-time reporting of the financial charges each application has incurred.

<!--more-->

Here’s why that’s important: more and more multi-application Kubernetes cloud deployments are being hosted by providers like AWS or Azure. These deployments are typically metered and billed as a single account – obscuring important information about specific application uses and impeding the adoption of accounting and planning best practices. This also makes it all but impossible to accurately implement chargebacks to multiple internal or external cost centers.  

As Kubernetes deployments grow, so does the accounting challenge. Web services companies that pay for online capacity in advance are being hit with significant overage bills when their traffic spikes unexpectedly. Pinterest, for example, was hit with a web services bill in 2018 that was $20 million higher than anticipated, according to [The Information](https://www.theinformation.com/articles/as-aws-use-soars-companies-surprised-by-cloud-bills).

Purser helps medium-to-large scale Kubernetes administrators avoid surprises like these by analyzing, in real-time, every container in a specific deployment, tallying both the services consumed and what they are costing. As a result, cluster administrators can understand their current expenditures at a granular level and plan more effectively.

The tool works by utilizing Kubernetes Custom Resource Definitions (CRDs) to support the creation of separate application “teams” for which Purser computes the associated financial costs. It tracks whenever a service is spun up or down and monitors how long each service has been in use. Those measurements are correlated with the appropriate web service (e.g. AWS or Azure) rate card to calculate real-time financial expenditures for each application/team. Purser is the only open source tool that offers this specific functionality.

Overall, Purser can provide visibility into the following aspects of a Kubernetes cluster:

- workload costs associated with native/custom resources consumed
- savings opportunities associated with storage and compute requirements
- single-pane view into the complete cluster hierarchy
- capacity allocations for CPU, memory, disk space, and other resources
- interactions among associated resources, such as pods and services

Purser began life in early 2018 as an internal VMware project. It was open-sourced around this time last year and received its [1.0 release last December](https://blogs.vmware.com/opensource/2018/12/13/purser-open-source/). It has gained significant momentum since then, earning 70+ GitHub stars and attracting both internal and external contributors.

The project retains its original, broad logistical-tracking functionality, and over the last six months, we have enhanced its UI and simplified installation by making it available through Helm chart. We’ve also added a showback/chargeback functionality which is now so popular that we are describing Purser primarily as an open source Kubernetes showback/chargeback tool. VMware’s own DevOps team now uses it for both cost assessments and estimates.

As we look ahead, we’re hoping to add cross-cloud cost comparisons – which will show how current costs for any deployment would either rise or fall if you used an alternative provider. We’re also planning to enable multi-instance installation in order to better support large scale deployments.

For more information, come [find us on GitHub](https://github.com/vmware/purser) or better yet, join us at [the Open Source Summit North America](https://events19.linuxfoundation.org/events/open-source-summit-north-america-2019/) where we’ll be [hosting a deep-dive session](https://events.linuxfoundation.org/events/open-source-summit-north-america-2019/program/schedule/) discussing Purser and demonstrating its use live. In the meantime, try it out yourself and let us know if there’s anything you’d like us to add or if you’d like to join our team.

Stay tuned to the [Open Source Blog](https://blogs.vmware.com/opensource/) and follow us on Twitter ([@vmwopensource](https://twitter.com/vmwopensource)) for the latest features and updates from the VMware OSTC.
