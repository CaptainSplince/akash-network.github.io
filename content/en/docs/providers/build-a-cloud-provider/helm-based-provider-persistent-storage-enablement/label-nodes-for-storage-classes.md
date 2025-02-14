---
title: "Label Nodes For Storage Classes"
key: "label-nodes-for-storage-classes"
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
        parent: "helm-based-provider-persistent-storage-enablement"

---
Label Nodes For Storage Classes
===============================

Each node serving persistent storage should have `akash.network/storageclasses` label set.

NOTE - currently the Helm Charts for persistent storage support only a single storageclass per cluster. All nodes in the cluster should be marked as `beta2` - as an example - and cannot have a mix of `beta2` and `beta3` nodes.

*   Ensure that this command is issued - one at a time - for all nodes serving persistent storage
*   Replace the `storageclasses` value with the proper storage class and as clarified in the example command

    kubectl label node <node-name> akash.network/storageclasses=<beta1|beta2|beta3> --overwrite
    

#### Example Label Command

*   In our example with a single node serving persistent storage with the storage class of beta2, the following label syntax would be applied.
    
        kubectl label node node2 akash.network/storageclasses=beta2 --overwrite