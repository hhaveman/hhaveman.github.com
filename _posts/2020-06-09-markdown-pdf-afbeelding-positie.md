---
layout: post
title: "Markdown PDF afbeelding positie"
description: ""
category: [markdown, pandoc]
tags: [markdown, pandoc]
---
{% include JB/setup %}


Als met Pandoc afbeeldingen worden meegegeven in een markdown document dan
worden de afbeeldingen standaard niet op de juiste positie weergegeven.

Om dit toch voor elkaar te krijgen moet de volgende optie meegegeven worden aan
Pandoc:

```bash

  -f markdown-implicit_figures

```

