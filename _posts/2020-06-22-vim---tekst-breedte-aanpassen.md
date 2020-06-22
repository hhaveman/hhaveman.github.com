---
layout: post
title: "Vim   Tekst breedte aanpassen"
description: ""
category:  [Vim]
tags: [vim]
---
{% include JB/setup %}


Tekst breedte van bijvoorbeeld een Markdown bestand kan worden aangepast door
het **gq** commando. De tekst breedte wordt dan weergegeven tot de
breedte van de *textwidth* variabele. 

Door de *formatoptions* setting aan te passen en er de waarde *a* aan toe te
voegen zal dit afkappen op de breedte van de tekst al tijdens het typen
gebeuren. Men kan dit opnemen in het .vimrc bestand als volgt:

```vim

set formatoptions+=a

```

