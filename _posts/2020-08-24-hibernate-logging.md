---
layout: post
title: "Hibernate logging"
description: "Hoe log je in Hibernate"
category: [database,hibernate]
tags: [database,hibernate]
---
{% include JB/setup %}

In Hibernate kun je de sql statements loggen.
Je kunt het volgende in de application.yaml opnemen om de statements te loggen
en formateren

```yaml

spring:
    jpa:
        hibernate:
            show-sql: false
            format-sql: true

```

Op deze wijze worden de gegenereerde sql statements gegenereerd. Echter krijg je
dan niet de waarde van de parameters te zien. Hiervoor kun je de java logging
gebruiken. Pas hiervoor de application.yaml als volgt aan:

```yaml

logging:
    level:
        org.hibernate.SQL: debug
        org.hibernate.type.descriptor.sql: trace

```

De eerste regel toont het sql statement. De tweede regel toont de parameter
waardes.

