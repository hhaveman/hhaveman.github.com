---
layout: post
title: "Oracle Auditing uit"
description: "Hoe zet je auditing uit in Oracle"
category: [database]
tags: [database,oracle]
---
{% include JB/setup %}


Als je in Oracle auditing hebt aangezet, maar je krijgt hem niet meer uit dan
kun je het volgende uitvoeren om alsnog de auditing uit te zetten:

```
    set ORACLE_SID=<Sid naam>

    sqlplus / as sysdba

    show parameter audit

    ...
    audit_trail   string db

    alter system set audit_trail=none scope=spfile

    shutdown abort

    startup

    exit

```


