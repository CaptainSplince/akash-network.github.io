---
title: "Enable strictARP in kube-proxy"
key: "enable-strictarp-in-kube-proxy"
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
        parent: "ip-leases-provider-enablement-(optional-step)"

---
Enable strictARP in kube-proxy
==============================

If you’re using kube-proxy in IPVS mode, since Kubernetes v1.14.2 you have to enable strict ARP mode.

> _**NOTE**_ - this is not needed if you’re using kube-router as service-proxy because it is enabling strict ARP by default.

Achieve this by patching your kube-proxy config in current cluster:

    # see what changes would be made, returns nonzero returncode if different
    kubectl get configmap kube-proxy -n kube-system -o yaml | \
    sed -e "s/strictARP: false/strictARP: true/" | \
    kubectl diff -f - -n kube-system
    
    # actually apply the changes, returns nonzero returncode on errors only
    kubectl get configmap kube-proxy -n kube-system -o yaml | \
    sed -e "s/strictARP: false/strictARP: true/" | \
    kubectl apply -f - -n kube-system
    

*   If using kubespray for your cluster deployment, make sure to add the following variable:

    kube_proxy_strict_arp: true