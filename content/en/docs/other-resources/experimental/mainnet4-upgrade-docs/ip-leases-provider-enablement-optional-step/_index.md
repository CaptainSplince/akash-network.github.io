---
title: "IP Leases - Provider Enablement (Optional Step)"
key: "ip-leases-provider-enablement-(optional-step)"
description: ""
lead: ""
date: Thu Dec 29 2022 03:03:46 GMT-0800 (Pacific Standard Time)
lastmod: Thu Dec 29 2022 03:03:46 GMT-0800 (Pacific Standard Time)
draft: false
images: []
weight: 1
toc: true

menu:
    docs:
        parent: "build-a-cloud-provider"

---
IP Leases - Provider Enablement (Optional Step)
===============================================

In this guide we detail the enablement of IP Leases on a pre-existing Akash provider.

Please be aware of the following prerequisites prior to getting started.

> _**NOTE**_ - IP Leases enablement is an optional step for Akash providers. Some providers may not have available public IP address pools and/or other requirements for enabling this feature.

Prerequisites
-------------

*   Provider IP Leases enablement is only supported for Akash providers built using [Helm Charts](../../../../providers/build-a-cloud-provider/akash-cloud-provider-build-with-helm-charts/)
*   Available pool of unallocated public IP addresses

Sections in this Guide
----------------------

*   [Akash Provider Update](akash-provider-update.md)
*   [IP Operator](ip-operator.md)
*   [Create the MetalLB Namespace](create-the-metallb-namespace.md)
*   [MetalLB Install](metallb-install.md)
*   [Enable strictARP in kube-proxy](enable-strictarp-in-kube-proxy.md)
*   [Additional notes on the IP Operator](additional-notes-on-the-ip-operator.md)