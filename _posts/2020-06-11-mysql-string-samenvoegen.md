---
layout: post
title: "MySQL string samenvoegen"
description: ""
category: [database,mysql]
tags: [mysql,database]
---
{% include JB/setup %}



Normaal gesproken voeg je in SQL twee teksten samen door een dubbele pijp
symbool als volgt:

```sql

select a || b from c;

```

MySQL echter kent deze constructie niet. Voor MySQL kan de functie concat worden
gebruikt als volgt:

```sql

select concat(a,b) from c;

```

