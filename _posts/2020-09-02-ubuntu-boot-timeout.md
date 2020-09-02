---
layout: post
title: "Ubuntu boot timeout"
description: "Bij vagrant up kun het lang duren voor een verbinding gemaakt kan
worden"
category:  [vagrant,ubuntu,systemd]
tags: [vagrant,ubuntu,systemd]
---
{% include JB/setup %}

Als je Vagrant gebruikt met een Ubuntu box kan het zijn dat het lang duurt voor
de machine opkomt. je ziet ook vaak een melding langskomen dat er met ssh geen
verbinding gemaakt kan worden met de box.

Dit komt doordat Ubuntu tijdens het booten wacht totdat hij het netwerk gereed
ziet. Dit gebeurt niet en er treedt een timeout op van 90 seconden. Dit zal zich
een aantal malen herhalen voor Ubuntu verder gaat met booten.

Dit kan opgelost worden door in systemd een service timeout te definiëren. Dat
kan als volgt gebeuren:

```bash

  ln -s /dev/null /etc/systemd/system/systemd-networkd-wait-online.service

```
