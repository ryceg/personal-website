---
# Featured tags need to have the `list` layout.
layout: about

# The title of the tag's page.
title: Works

# The name of the tag, used in a post's front matter (e.g. tags: [<slug>]).
slug: Works

# (Optional) Write a short (~150 characters) description of this featured tag.
description: >
  My music, in sheet music, audio, visual, code, or purely conceptual forms.
---

{% for works in site.works %}
  <h2><a href="{{ works.url }}">{{ works.title }}</a></h2>
  <h3>{{ works.instrumentation }} - {{ works.dateofcomposition }} - {{ works.length }}</h3>
  <p>{{ works.content | markdownify }}</p>
{% endfor %}

<h2><a href="{{ /list-of-works }}">List of works</a></h2>
{:.faded}