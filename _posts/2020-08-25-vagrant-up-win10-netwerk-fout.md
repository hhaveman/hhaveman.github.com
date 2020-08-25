---
layout: post
title: "Vagrant up Win10 netwerk fout"
description: "Hoe los je de problemen op bij Vagrant up op windows 10"
category: [vagrant,virtualbox]
tags: [vagrant,virtualbox]
---
{% include JB/setup %}


Op windows 10 kun je met Vagrant netwerkproblemen krijgen als je Vagrant up
geeft. Je krijgt dan een foutmelding in de geest van:

Stderr: VBoxManage.EXE: error: Failed to open/create then internal network: ...
VERR_INTNET_FLT_IF_NOT_FOUND


Voer het volgende uit om dit probleem (hopelijk) op te lossen:

* Open Windows Network Connections
* Right click on VirtualBox Host only adapter that created
* Choose properties
* Check "VirtualBox NDIS6 Bridged Networking driver"
* disable and Enable the adapter


Zie URL https://stackoverflow.com/questions/33725779/failed-to-open-create-the-internal-network-vagrant-on-windows10/33733454
