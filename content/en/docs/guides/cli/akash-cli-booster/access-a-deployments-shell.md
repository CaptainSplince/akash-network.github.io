---
title: "Access a Deployment’s Shell"
key: "access-a-deployment's-shell"
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
        parent: "akash-cli-booster"

---
Access a Deployment’s Shell
===========================

    akash_shell sh
    

#### Example/Expected Output

*   In this example the contents of the current directory are listed - via “ls” - to prove we are inside the deployment’s container

    root@ip-10-0-10-163:~/akash-tools/cli-booster[http://akash-sentry01.skynetvalidators.com:26657][deploymentone][4815131-1-1-web]$ akash_shell sh
    
    Enter keyring passphrase:
    Enter keyring passphrase:
    #
    # ls
    bin  boot  dev	docker-entrypoint.d  docker-entrypoint.sh  etc	home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var