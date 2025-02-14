---
title: "Review Bids"
key: "review-bids"
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
        parent: "streamlined-steps"

---
Review Bids
===========

List Bids Received from Providers
---------------------------------

    provider-services query market bid list
    

**Choose Provider**
-------------------

*   Note - in the following command we set the AKASH\_PROVIDER address and then reference the environment variable in subsequent commands (create lease, send manifest, etc)
*   Alternatively we could add the provider variable to the env.sh script and re-issue \*\*\`\*\*source env.sh\` . This would negate the need to include the \`--provider\` switch in subsequent commands.
*   Replace the provider-address variable with the preferred provider address

    AKASH_PROVIDER=<provider-address>
    

Create Lease
------------

    provider-services tx market lease create --provider $AKASH_PROVIDER
    

**Confirm Lease Creation**
--------------------------

    provider-services query market lease list