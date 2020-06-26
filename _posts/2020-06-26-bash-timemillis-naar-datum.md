---
layout: post
title: "Bash timemillis naar datum"
description: "Bash timemillis naar datum conversie"
category: i[linux,bash]
tags: [linux,bash]
---
{% include JB/setup %}


Soms heb je in _bash_ de tijd in milliseconden sinds 1970. Als je deze wil
omzetten naar de datum (of een ander tijdsaanduiding) kun je het commando _date_
gebruiken. De milliseconden geef je weer met een apestaart ervoor.

```bash

date --date @123456789

```

