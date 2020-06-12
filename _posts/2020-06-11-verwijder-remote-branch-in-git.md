---
layout: post
title: "Verwijder remote branch in Git"
description: ""
category: [git]
tags: [git]
---
{% include JB/setup %}

Om een branch in de remote repository te verwijderen moet je het volgende
uitvoeren:

```bash

git push origin --delete <Branch naam>

```

Als een remote branch is verwijderd, wordt hij niet automatisch bij iedereen
verwijderd. Hij moet bij iedereen nog afzonderlijk verwijderd worden. Dit kan
gedaan worden door het commando:

```bash

git fetch --all --prune

```

Het kan zo worden ingesteld dat dit automatisch gebeurd bij een fetch (en dus een
pull). Hiervoor moet de volgende configuratie aanpassing komen:

```bash

git config (--global) remote.origin.prune true

```

