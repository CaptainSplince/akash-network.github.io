---
title: "TLS Termination of Akash Deployments"
key: "tls-termination-of-akash-deployments"
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
        parent: "integrations"

---
TLS Termination of Akash Deployments
====================================

Overview
--------

Currently only self-signed certificates are available from Akash Providers.

In this guide we detail a Cloudflare TLS termination strategy which will give Akash deployments valid public certificates. Cloudflare will proxy traffic intended for the Akash deployment and allow end to end encrypted communication.

**STEP 1** - [Prerequisites](prerequisites.md)

**STEP 2** - [Akash with TLS Example](akash-with-tls-example.md)

**STEP 3** - [Find IP Address of Deployment](find-ip-address-of-deployment.md)

**STEP 4** - [Cloudflare Configuration](cloudflare-configuration.md)

**STEP 5** - [Verify HTTPS](verify-https.md)

**STEP 6** - [Troubleshooting](troubleshooting.md)