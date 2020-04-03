---
layout: post
tags: purser
date: 2018-05-25 
thumbnail: https://user-images.githubusercontent.com/42761785/53145168-2f4e4980-35c5-11e9-867b-8d637671ec23.png
title: Purser: Visibility into Cloud Native Applications
published: true
---

*As posted on [blogs.vmware.com](https://blogs.vmware.com/opensource/2018/12/13/purser-open-source/) on December 13, 2018*

Kubernetes clusters can be challenging to monitor. With applications decomposed into microservices and then deployed across many Kubernetes clusters –and pods within those clusters– it’s not a simple task to keep track of what’s happening, where. It’s this challenge that inspired Purser.

<!--more-->

## About Purser
A purser is the individual responsible for keeping track of all financial and logistical matters aboard ship. [Project Purser](https://github.com/vmware/purser), open sourced this week, enables users to act as the “purser” for their Kubernetes environment. Purser lets users easily monitor and draw insights into the Kubernetes infrastructure built atop any cloud platform for their cloud native applications.

[Purser](https://github.com/vmware/purser) is designed as an extension to Kubernetes. It provides an insight into cloud native application workloads. With its vibrant user interface, visibility into your cluster hierarchy, capacity allocations, and resource interactions are all available in a single glance.

Purser seamlessly integrates with `kubectl` to provide more granular details such as the cost associated with workloads, savings opportunities and customized logical grouping of resources for enhanced filtering. Purser also provides RESTful APIs for easy extension and customization for your needs.

Whether you are a sysadmin trying to monitor Kubernetes cluster performance or troubleshooting issues, a DevOps engineer trying to monitor and optimize cluster operations and deployments, or a Developer wanting to view their workloads, Purser is a handy tool for all.

## Initial Purser release highlights
The [first release](https://github.com/vmware/purser/releases/tag/v1.0.0) comes loaded with the capability to provide visibility into the following aspects of the K8s cluster:

- workload cost associated with the K8s native/custom resources
- savings opportunities associated with storage and compute requirements
- single view of the complete cluster hierarchy
- capacity allocations for CPU, memory and disk space
- interactions among associated resources such as pods and services

As the initial developers of Purser, we are very excited about the project – but are even more excited to release this to the open source community. We invite you to join the project as contributors.
So give it a [try](https://github.com/vmware/purser) today, help build a new community, and tell us what you think on our [GitHub page](https://github.com/vmware/purser).
